---
title: Поддержка шаблонов элементов управления в поставщике модели автоматизации пользовательского интерфейса
description: В этом разделе показано, как поставщик автоматизации пользовательского интерфейса Майкрософт реализует шаблоны элементов управления для элемента управления. Шаблоны элементов управления позволяют клиентским приложениям управлять элементом управления и получать сведения о нем.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54e75fa12dba891bc4eded5fd9763f7825eb7f88
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "104335400"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a><span data-ttu-id="03dd1-104">Поддержка шаблонов элементов управления в поставщике модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="03dd1-104">Support Control Patterns in a UI Automation Provider</span></span>

<span data-ttu-id="03dd1-105">В этом разделе показано, как поставщик автоматизации пользовательского интерфейса Майкрософт реализует шаблоны элементов управления для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="03dd1-105">This topic shows how a Microsoft UI Automation provider implements control patterns for a control.</span></span> <span data-ttu-id="03dd1-106">Шаблоны элементов управления позволяют клиентским приложениям управлять элементом управления и получать сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="03dd1-106">Control patterns enable client applications to manipulate the control and get information about it.</span></span>

<span data-ttu-id="03dd1-107">Поставщик реализует шаблон элемента управления, выполнив следующие основные действия.</span><span class="sxs-lookup"><span data-stu-id="03dd1-107">A provider implements a control pattern by following these main steps:</span></span>

1.  <span data-ttu-id="03dd1-108">Реализуйте интерфейс поставщика, который поддерживает шаблон элемента управления.</span><span class="sxs-lookup"><span data-stu-id="03dd1-108">Implement the provider interface that supports the control pattern.</span></span> <span data-ttu-id="03dd1-109">Например, для поддержки шаблона элемента управления [Selection](uiauto-implementingselection.md) поставщик для пользовательского элемента управления "список" будет реализовывать интерфейс [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="03dd1-109">For example, to support the [Selection](uiauto-implementingselection.md) control pattern, a provider for a custom list control would implement the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>
2.  <span data-ttu-id="03dd1-110">Возвращает объект, содержащий интерфейс поставщика шаблона элемента управления, когда модель автоматизации пользовательского интерфейса вызывает метод [**иравелементпровидерсимпле:: жетпаттернпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) поставщика.</span><span class="sxs-lookup"><span data-stu-id="03dd1-110">Return an object that contains the control pattern provider interface when UI Automation calls the provider's [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) method.</span></span>

<span data-ttu-id="03dd1-111">В следующем примере показана реализация интерфейса [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) для пользовательского элемента управления списка с одним выбором.</span><span class="sxs-lookup"><span data-stu-id="03dd1-111">The following example shows the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface implementation for a custom, single-selection list control.</span></span> <span data-ttu-id="03dd1-112">Реализация включает методы получения свойств для свойств Исселектионрекуиред и Канселектмултипле, а также метод для получения поставщика для выбранного элемента списка.</span><span class="sxs-lookup"><span data-stu-id="03dd1-112">The implementation includes property-retrieval methods for the IsSelectionRequired and CanSelectMultiple properties, and a method for retrieving the provider for the selected list item.</span></span>


```C++
// Specifies whether the list control supports the selection of
// multiple items at the same time.
IFACEMETHODIMP ListProvider::get_CanSelectMultiple(BOOL *pRetVal)
{
    *pRetVal = FALSE;
    return S_OK;
} 

// Specifies whether the list must have an item selected at all times.
IFACEMETHODIMP ListProvider::get_IsSelectionRequired(BOOL *pRetVal)
{
   *pRetVal = TRUE;
   return S_OK;
}

// Retrieves the provider of the selected item in a custom list control. 
//
// m_pControl - pointer to an application-defined object for managing
//   the custom list control. 
//
// ListItemProvider - application-defined class that inherits the 
//   IRawElementProviderSimple interface.
//
// GetItemProviderByIndex - application-defined method that retrieves the 
//   IRawElementProviderSimple interface of the selected item.
IFACEMETHODIMP ListProvider::GetSelection(SAFEARRAY** pRetVal)
{
    // Create a safe array to store the IRawElementProviderSimple pointer.
    SAFEARRAY *psa = SafeArrayCreateVector(VT_UNKNOWN, 0, 1);

    // Retrieve the index of the selected list item. 
    int index = m_pControl->GetSelectedIndex(); 

    // Retrieve the IRawElementProviderSimple pointer of the selected list
    // item. ListItemProvider is an application-defined class that 
    // inherits the IRawElementProviderSimple interface. 
    ListItemProvider* pItem = GetItemProviderByIndex(index); 
    if (pItem != NULL)
    {
        LONG i = 0;
        SafeArrayPutElement(psa, &i, pItem);
    }
    *pRetVal = psa;
    return S_OK;
}
```



<span data-ttu-id="03dd1-113">В следующем примере показана реализация [**иравелементпровидерсимпле:: жетпаттернпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) , которая возвращает объект, реализующий [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="03dd1-113">The following example shows an implementation of [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) that returns an object that implements [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span> <span data-ttu-id="03dd1-114">Большинство элементов управления "список" также поддерживают другие шаблоны, но в этом примере возвращается пустая ссылка для всех других идентификаторов шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="03dd1-114">Most list controls would support other patterns as well, but this example returns a null reference for all other control pattern identifiers.</span></span>


```C++
// Retrieves an object that supports the control pattern provider interface 
// for the specified control pattern. 
IFACEMETHODIMP ListProvider::GetPatternProvider(PATTERNID patternId, IUnknown** pRetVal)
{
    *pRetVal = NULL;
    if (patternId == UIA_SelectionPatternId) 
    {
        // Return the object that implements ISelectionProvider. In this example, 
        // ISelectionProvider is implemented in the current object (this).
        *pRetVal = static_cast<IRawElementProviderSimple*>(this);
        AddRef();  
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="03dd1-115">См. также</span><span class="sxs-lookup"><span data-stu-id="03dd1-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="03dd1-116">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="03dd1-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="03dd1-117">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="03dd1-117">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="03dd1-118">Разделы руководства для поставщиков автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="03dd1-118">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




