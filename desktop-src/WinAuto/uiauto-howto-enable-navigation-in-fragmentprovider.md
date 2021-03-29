---
title: Как включить навигацию в поставщике фрагментов автоматизации пользовательского интерфейса
description: Этот раздел содержит пример кода, демонстрирующий, как включить навигацию в поставщике Microsoft UI Automation для элемента в фрагменте.
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067449"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a><span data-ttu-id="82ece-103">Как включить навигацию в поставщике фрагментов автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="82ece-103">How to Enable Navigation in a UI Automation Fragment Provider</span></span>

<span data-ttu-id="82ece-104">Этот раздел содержит пример кода, демонстрирующий, как включить навигацию в поставщике Microsoft UI Automation для элемента в фрагменте.</span><span class="sxs-lookup"><span data-stu-id="82ece-104">This topic contains example code that shows how to enable navigation in a Microsoft UI Automation provider for an element in a fragment.</span></span>

<span data-ttu-id="82ece-105">В следующем примере кода реализуется метод [**иравелементпровидерфрагмент:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) для элемента списка в пользовательском элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="82ece-105">The following example code implements the [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method for a list item in a custom list control.</span></span> <span data-ttu-id="82ece-106">Родительский элемент — это пользовательский элемент управления "список", а родственные элементы — это другие элементы в списке.</span><span class="sxs-lookup"><span data-stu-id="82ece-106">The parent element is the custom list control, and the sibling elements are other items in the list.</span></span> <span data-ttu-id="82ece-107">Метод задает для параметра *Претвал* **значение NULL** , если в указанном направлении нет элемента.</span><span class="sxs-lookup"><span data-stu-id="82ece-107">The method sets the *pRetVal* parameter to **NULL** if there is no element in the specified direction.</span></span>


```C++
// Implementation of IRawElementProviderFragment::Navigate.
// Enables UI Automation to locate the element in the tree.
HRESULT STDMETHODCALLTYPE ListItemProvider::Navigate(NavigateDirection direction, IRawElementProviderFragment ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }

    IRawElementProviderFragment* pFrag = NULL;
    switch(direction)
    {
        case NavigateDirection_Parent:
            pFrag = (IRawElementProviderFragment*) m_parentProvider;       
            break;

        case NavigateDirection_NextSibling:
            pFrag = (IRawElementProviderFragment*) m_nextSiblingProvider;
            break;

        case NavigateDirection_PreviousSibling:  
            pFrag = (IRawElementProviderFragment*) m_previousSiblingProvider;
            break;
    }
    *pRetVal = pFrag;
    if (pFrag != NULL) 
    {
        pFrag->AddRef();
    }
    return S_OK;
}              
```



## <a name="related-topics"></a><span data-ttu-id="82ece-108">См. также</span><span class="sxs-lookup"><span data-stu-id="82ece-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="82ece-109">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="82ece-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="82ece-110">Реализация поставщика автоматизации пользовательского интерфейса Server-Side</span><span class="sxs-lookup"><span data-stu-id="82ece-110">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="82ece-111">Разделы руководства для поставщиков автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="82ece-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




