---
title: Использование модели автоматизации пользовательского интерфейса для обеспечения доступа к безоконному элементу управления ActiveX
description: Описывает, как использовать автоматизацию пользовательского интерфейса Майкрософт \ 32; API, чтобы обеспечить доступность элемента управления Microsoft ActiveX без окон для клиентских приложений с поддержкой специальных возможностей (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Безоконный элемент управления ActiveX, Специальные возможности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ada1d26463b0654c1808f6e4fd43f571687d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792463"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="6e365-104">Использование модели автоматизации пользовательского интерфейса для обеспечения доступа к безоконному элементу управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="6e365-104">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>

<span data-ttu-id="6e365-105">Описание использования API Microsoft UI Automation для обеспечения доступности элемента управления Microsoft ActiveX без окон для клиентских приложений с поддержкой специальных возможностей (AT).</span><span class="sxs-lookup"><span data-stu-id="6e365-105">Describes how to use the Microsoft UI Automation API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6e365-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="6e365-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6e365-107">Технологии</span><span class="sxs-lookup"><span data-stu-id="6e365-107">Technologies</span></span>

-   [<span data-ttu-id="6e365-108">Элементы управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="6e365-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="6e365-109">Модель автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="6e365-109">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="6e365-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="6e365-110">Prerequisites</span></span>

-   <span data-ttu-id="6e365-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="6e365-111">C/C++</span></span>
-   <span data-ttu-id="6e365-112">Программирование Microsoft Win32 и объектной модели компонентов (COM)</span><span class="sxs-lookup"><span data-stu-id="6e365-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="6e365-113">Элементы управления ActiveX без окон</span><span class="sxs-lookup"><span data-stu-id="6e365-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="6e365-114">Поставщики автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="6e365-114">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="6e365-115">Инструкции</span><span class="sxs-lookup"><span data-stu-id="6e365-115">Instructions</span></span>

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a><span data-ttu-id="6e365-116">Шаг 1. Реализация интерфейсов поставщика автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6e365-116">Step 1: Implement the UI Automation provider interfaces.</span></span>

<span data-ttu-id="6e365-117">Чтобы сделать приложение доступным, необходимо реализовать интерфейсы поставщика автоматизации пользовательского интерфейса для безоконного элемента управления ActiveX, включая [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**иравелементпровидерфрагментрут**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)и [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span><span class="sxs-lookup"><span data-stu-id="6e365-117">To make your application accessible, you must implement the UI Automation provider interfaces for your windowless ActiveX control, including [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), and [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span></span> <span data-ttu-id="6e365-118">Эти интерфейсы следует реализовать так же, как для элемента управления на основе окна, за исключением описанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="6e365-118">You should implement these interfaces just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="6e365-119">Дополнительные сведения о реализации интерфейсов поставщика UIA см. в разделе [Справочник программиста поставщика автоматизации пользовательского интерфейса](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="6e365-119">For more information about implementing UIA provider interfaces, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="6e365-120">Шаг 2. Реализация интерфейса IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="6e365-120">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="6e365-121">Когда клиенту требуются сведения о специальных возможностях элемента управления без окон, контейнер элементов управления вызывает метод **IServiceProvider:: QueryService** элемента управления, чтобы получить указатель интерфейса [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6e365-121">When a client needs accessibility information about your windowless control, the control container calls your control's **IServiceProvider::QueryService** method to retrieve the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface pointer for your control.</span></span>

<span data-ttu-id="6e365-122">В следующем примере показано, как реализовать метод **QueryService** .</span><span class="sxs-lookup"><span data-stu-id="6e365-122">The following example shows how to implement the **QueryService** method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a><span data-ttu-id="6e365-123">Шаг 3. Реализация метода Иравелементпровидерфрагмент:: Navigate.</span><span class="sxs-lookup"><span data-stu-id="6e365-123">Step 3: Implement the IRawElementProviderFragment::Navigate method.</span></span>

<span data-ttu-id="6e365-124">При вызове метода [**иравелементпровидерфрагмент:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) элемента управления без окон для перехода к родительскому поставщику элемента управления без окон метод **navigate** должен делегировать методу [**иравелементпровидервиндовлесссите:: жетаджацентфрагмент**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) контейнера элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6e365-124">When your windowless control’s [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method is called to navigate to the parent or a sibling of the windowless control's root provider, your **Navigate** method should delegate to the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method of the control container.</span></span>

<span data-ttu-id="6e365-125">В следующем примере показано, как реализовать метод [**navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="6e365-125">The following example shows how to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a><span data-ttu-id="6e365-126">Шаг 4. Реализация метода Иравелементпровидерфрагмент:: Жетрунтимеид.</span><span class="sxs-lookup"><span data-stu-id="6e365-126">Step 4: Implement the IRawElementProviderFragment::GetRuntimeId method.</span></span>

<span data-ttu-id="6e365-127">Когда безоконный элемент управления получает вызов своего метода [**иравелементпровидерфрагмент:: жетрунтимеид**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) , элемент управления должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6e365-127">When your windowless control receives a call to its [**IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) method, the control must do the following:</span></span>

1.  <span data-ttu-id="6e365-128">Получите префикс идентификатора среды выполнения, вызвав метод [**иравелементпровидервиндовлесссите:: жетрунтимеидпрефикс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) сайта управления.</span><span class="sxs-lookup"><span data-stu-id="6e365-128">Retrieve a runtime ID prefix by calling the control site's [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>
2.  <span data-ttu-id="6e365-129">Создайте уникальный идентификатор среды выполнения для элемента управления, добавив целое число в префикс идентификатора среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="6e365-129">Create a unique runtime ID for the control by appending an integer to the runtime ID prefix.</span></span>
3.  <span data-ttu-id="6e365-130">Верните идентификатор среды выполнения вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="6e365-130">Return the runtime ID to the caller.</span></span>

<span data-ttu-id="6e365-131">В следующем примере показано, как реализовать метод [**жетрунтимеид**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) .</span><span class="sxs-lookup"><span data-stu-id="6e365-131">The following example shows how to implement the [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a><span data-ttu-id="6e365-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6e365-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e365-133">Использование MSAA для обеспечения возможности доступа к безоконному элементу управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="6e365-133">Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="6e365-134">Специальные возможности элемента управления ActiveX без окон</span><span class="sxs-lookup"><span data-stu-id="6e365-134">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 