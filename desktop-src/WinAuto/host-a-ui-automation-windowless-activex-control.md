---
title: Размещение элемента управления ActiveX без окна модели автоматизации пользовательского интерфейса
description: Узнайте, как создать контейнер элементов управления, который может размещать элементы управления Microsoft ActiveX без окон, реализующие автоматизацию пользовательского интерфейса Майкрософт.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- Модель автоматизации пользовательского интерфейса, безоконный элемент управления ActiveX
- Безоконный элемент управления ActiveX, модель автоматизации пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337681"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a><span data-ttu-id="c2bbd-105">Размещение элемента управления ActiveX без окна модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c2bbd-105">Host a UI Automation Windowless ActiveX Control</span></span>

<span data-ttu-id="c2bbd-106">Узнайте, как создать контейнер элементов управления, который может размещать элементы управления Microsoft ActiveX без окон, реализующие автоматизацию пользовательского интерфейса Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-106">Learn how to create a control container that can host windowless Microsoft ActiveX controls that implement Microsoft UI Automation.</span></span> <span data-ttu-id="c2bbd-107">С помощью описанных здесь действий можно убедиться, что любые элементы управления без окон автоматизации пользовательского интерфейса, размещенные в контейнере управления, доступны для клиентских приложений с поддержкой специальных возможностей (AT).</span><span class="sxs-lookup"><span data-stu-id="c2bbd-107">By using the steps described here, you can ensure that any UI Automation windowless controls that are hosted in your control container are accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c2bbd-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="c2bbd-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c2bbd-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="c2bbd-109">Technologies</span></span>

-   [<span data-ttu-id="c2bbd-110">Элементы управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c2bbd-110">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="c2bbd-111">Модель автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c2bbd-111">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="c2bbd-112">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="c2bbd-112">Prerequisites</span></span>

-   <span data-ttu-id="c2bbd-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="c2bbd-113">C/C++</span></span>
-   <span data-ttu-id="c2bbd-114">Программирование Microsoft Win32 и объектной модели компонентов (COM)</span><span class="sxs-lookup"><span data-stu-id="c2bbd-114">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="c2bbd-115">Элементы управления ActiveX без окон</span><span class="sxs-lookup"><span data-stu-id="c2bbd-115">Windowless ActiveX controls</span></span>
-   <span data-ttu-id="c2bbd-116">Поставщики автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c2bbd-116">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="c2bbd-117">Инструкции</span><span class="sxs-lookup"><span data-stu-id="c2bbd-117">Instructions</span></span>

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a><span data-ttu-id="c2bbd-118">Шаг 1. предоставление интерфейса Иравелементпровидерсимпле от имени элемента управления без окон.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-118">Step 1: Provide the IRawElementProviderSimple interface on behalf of the windowless control.</span></span>

<span data-ttu-id="c2bbd-119">Всякий раз, когда системе требуется указатель [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для корневого элемента управления без окон, система запрашивает контейнер элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-119">Whenever the system needs the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer for the root of a windowless control, the system queries the control container.</span></span> <span data-ttu-id="c2bbd-120">Для получения указателя контейнер вызывает реализацию метода [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) элемента управления без окон.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-120">To retrieve the pointer, the container calls the windowless control's implementation of the [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>

<span data-ttu-id="c2bbd-121">Если контейнер элемента управления имеет реализацию модели автоматизации пользовательского интерфейса, он может вернуть в систему указатель [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) элемента управления без окон.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-121">If the control container has a UI Automation implementation, it can return the windowless control's [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer to the system.</span></span>

<span data-ttu-id="c2bbd-122">Если контейнер элемента управления имеет реализацию Microsoft Active Accessibility, вызовите функцию [**уиаиакцессиблефромпровидер**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) , чтобы получить указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , представляющий элемент управления, а затем верните указатель интерфейса **IAccessible** в систему.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-122">If the control container has a Microsoft Active Accessibility implementation, call the [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) function to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer that represents the control, and then return the **IAccessible** interface pointer to the system.</span></span>

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a><span data-ttu-id="c2bbd-123">Шаг 2. Реализация интерфейса Иравелементпровидервиндовлесссите.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-123">Step 2: Implement the IRawElementProviderWindowlessSite interface.</span></span>

<span data-ttu-id="c2bbd-124">Контейнер элемента управления реализует интерфейс [**иравелементпровидервиндовлесссите**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) , позволяющий использовать безоконный элемент управления, основанный на модели автоматизации пользовательского интерфейса, для передачи сведений о специальных возможностях.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-124">A control container implements the [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) interface enable a windowless control that is based on UI Automation to communicate its accessibility information.</span></span>

1.  <span data-ttu-id="c2bbd-125">Реализуйте [**иравелементпровидервиндовлесссите:: жетрунтимеидпрефикс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span><span class="sxs-lookup"><span data-stu-id="c2bbd-125">Implement [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span></span>

    <span data-ttu-id="c2bbd-126">Фрагмент управления без окон должен создать уникальный идентификатор среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-126">A windowless control fragment must create a unique runtime ID for itself.</span></span> <span data-ttu-id="c2bbd-127">Чтобы создать идентификатор среды выполнения, фрагмент управления без окон извлекает значение префикса путем вызова метода [**жетрунтимеидпрефикс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) сайта элемента управления, а затем добавляет к префиксу целочисленное значение, уникальное относительно всех остальных фрагментов в безоконном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-127">To create its runtime ID, a windowless control fragment retrieves a prefix value by calling the control site's [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method, and then appends to the prefix an integer value that is unique relative to all other fragments in the windowless control.</span></span>

    <span data-ttu-id="c2bbd-128">Сайт управления для элемента управления без окон должен реализовывать метод [**жетрунтимеидпрефикс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) , формируя **массив SafeArray** , содержащий константу **уиааппендрунтимеид**, за которым следует целочисленное значение, уникальное для сайта.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-128">The control site for a windowless control should implement the [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method by forming a **SAFEARRAY** that contains the constant **UiaAppendRuntimeId**, followed by an integer value that is unique to the site.</span></span>

    <span data-ttu-id="c2bbd-129">В этом примере показано, как вернуть префикс идентификатора среды выполнения для элемента управления без окон.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-129">This example shows how to return a runtime ID prefix for a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  <span data-ttu-id="c2bbd-130">Реализуйте метод [**иравелементпровидервиндовлесссите:: жетаджацентфрагмент**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .</span><span class="sxs-lookup"><span data-stu-id="c2bbd-130">Implement the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method.</span></span>

    <span data-ttu-id="c2bbd-131">Элемент управления, реализующий автоматизацию пользовательского интерфейса, должен возвращать указатель на родительский поставщик фрагментов элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-131">A control that implements UI Automation must return a pointer to the control's parent fragment provider.</span></span>

    <span data-ttu-id="c2bbd-132">Чтобы получить родительский элемент фрагмента, объект, реализующий интерфейс [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) , должен иметь возможность реализовать метод [**navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="c2bbd-132">To return the parent of the fragment, an object that implements the [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) interface must be able to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span> <span data-ttu-id="c2bbd-133">Реализовать **навигацию** для безоконного элемента управления сложно, поскольку элемент управления может не определить его расположение в доступном дереве родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-133">Implementing **Navigate** is difficult for a windowless control because the control might be unable to determine its location in the accessible tree of the parent object.</span></span> <span data-ttu-id="c2bbd-134">Метод [**иравелементпровидервиндовлесссите:: жетаджацентфрагмент**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) позволяет безоконному элементу управления запрашивать его сайт для смежного фрагмента, а затем возвращать этот фрагмент клиенту, который вызвал команду **navigate**.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-134">The [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method enables the windowless control to query its site for the adjacent fragment, and then return that fragment to the client that called **Navigate**.</span></span>

    <span data-ttu-id="c2bbd-135">В этом примере показано, как контейнер элемента управления Извлекает родительский фрагмент элемента управления без окон.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-135">This example shows how a control container retrieves the parent fragment of a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a><span data-ttu-id="c2bbd-136">Шаг 3. необязательно. Реализация интерфейса Иравелементпровидерхостингакцессиблес.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-136">Step 3: Optional: Implement the IRawElementProviderHostingAccessibles interface.</span></span>

<span data-ttu-id="c2bbd-137">Реализуйте интерфейс [**иравелементпровидерхостингакцессиблес**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) , если контейнер элемента управления имеет реализацию поставщика автоматизации пользовательского интерфейса, которая является корнем дерева специальных возможностей, включающего элементы управления ActiveX без окон, поддерживающие Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-137">Implement the [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) interface if your control container has a UI Automation provider implementation that is the root of an accessibility tree that includes windowless ActiveX controls that support Microsoft Active Accessibility.</span></span> <span data-ttu-id="c2bbd-138">Интерфейс **иравелементпровидерхостингакцессиблес** содержит один метод [**жетембеддедакцессиблес**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), который получает указатели интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) всех безоконных элементов управления ActiveX, работающих в Microsoft Active Accessibility, размещенных в контейнере элементов управления.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-138">The **IRawElementProviderHostingAccessibles** interface has a single method, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), which retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers of all Microsoft Active Accessibility-based windowless ActiveX controls that are hosted by your control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2bbd-139">См. также</span><span class="sxs-lookup"><span data-stu-id="c2bbd-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2bbd-140">Размещение элемента управления ActiveX без окна MSAA</span><span class="sxs-lookup"><span data-stu-id="c2bbd-140">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[<span data-ttu-id="c2bbd-141">Специальные возможности элемента управления ActiveX без окон</span><span class="sxs-lookup"><span data-stu-id="c2bbd-141">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 