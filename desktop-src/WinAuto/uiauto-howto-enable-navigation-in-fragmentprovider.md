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
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a>Как включить навигацию в поставщике фрагментов автоматизации пользовательского интерфейса

Этот раздел содержит пример кода, демонстрирующий, как включить навигацию в поставщике Microsoft UI Automation для элемента в фрагменте.

В следующем примере кода реализуется метод [**иравелементпровидерфрагмент:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) для элемента списка в пользовательском элементе управления "список". Родительский элемент — это пользовательский элемент управления "список", а родственные элементы — это другие элементы в списке. Метод задает для параметра *Претвал* **значение NULL** , если в указанном направлении нет элемента.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Реализация поставщика автоматизации пользовательского интерфейса Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Разделы руководства для поставщиков автоматизации пользовательского интерфейса](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




