---
title: Пошаговое руководство по дереву модели автоматизации пользовательского интерфейса
description: В этом разделе содержится пример кода, демонстрирующий использование интерфейса Иуиаутоматионтривалкер для пошагового изучения элементов в дереве Microsoft UI Automation.
ms.assetid: 41ca783d-56d1-4ad5-8f07-c265ff2e07bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fe6539a24f271f5c1e8042b1be9933a77f1118b27730d510026de1852d7938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324452"
---
# <a name="how-to-walk-the-ui-automation-tree"></a>Пошаговое руководство по дереву модели автоматизации пользовательского интерфейса

В этом разделе содержится пример кода, демонстрирующий использование интерфейса [**иуиаутоматионтривалкер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) для пошагового изучения элементов в дереве Microsoft UI Automation. В нем рассматриваются следующие темы:

-   [Проход по потомкам элемента](#walking-through-descendants-of-an-element)
-   [Проход по элементам предка](#walking-through-ancestor-elements)
-   [Связанные темы](#related-topics)

## <a name="walking-through-descendants-of-an-element"></a>Проход по потомкам элемента

Следующий пример кода является рекурсивной функцией, которая проходит через все потомки элемента пользовательского интерфейса и отображает их типы элементов управления в иерархическом списке.


```C++
// CAUTION: Do not pass in the root (desktop) element. Traversing the entire subtree
// of the desktop could take a very long time and even lead to a stack overflow.
void ListDescendants(IUIAutomationElement* pParent, int indent)
{
    if (pParent == NULL)
        return;

    IUIAutomationTreeWalker* pControlWalker = NULL;
    IUIAutomationElement* pNode = NULL;

    g_pAutomation->get_ControlViewWalker(&pControlWalker);
    if (pControlWalker == NULL)
        goto cleanup;

    pControlWalker->GetFirstChildElement(pParent, &pNode);
    if (pNode == NULL)
        goto cleanup;

    while (pNode)
    {
        BSTR desc;
        pNode->get_CurrentLocalizedControlType(&desc);
        for (int x = 0; x <= indent; x++)
        {
            std::wcout << L"   ";
        }
        std::wcout << desc << L"\n";
        SysFreeString(desc);

        ListDescendants(pNode, indent+1);
        IUIAutomationElement* pNext;
        pControlWalker->GetNextSiblingElement(pNode, &pNext);
        pNode->Release();
        pNode = pNext;
    }

cleanup:
    if (pControlWalker != NULL)
        pControlWalker->Release();

    if (pNode != NULL)
        pNode->Release();

    return;
}
```



## <a name="walking-through-ancestor-elements"></a>Проход по элементам предка

В следующем примере кода показана функция, которая проходит через предков элемента для указания родительского элемента. Это полезно, если необходимо найти родительское окно элемента управления. Функция возвращает **значение NULL** для элементов верхнего уровня; то есть элементы, родительским элементом которых является Рабочий стол.


```C++
IUIAutomationElement* GetContainingWindow(IUIAutomationElement* pChild)
{

    if (pChild == NULL)
        return NULL;

    IUIAutomationElement* pDesktop = NULL;
    HRESULT hr = g_pAutomation->GetRootElement(&pDesktop);
    if (FAILED(hr))
        return NULL;

    BOOL same;
    g_pAutomation->CompareElements(pChild, pDesktop, &same);
    if (same)
    {
        pDesktop->Release();
        return NULL; // No parent, so return NULL.
    }

    IUIAutomationElement* pParent = NULL;
    IUIAutomationElement* pNode = pChild;

    // Create the treewalker.
    IUIAutomationTreeWalker* pWalker = NULL;
    g_pAutomation->get_ControlViewWalker(&pWalker);
    if (pWalker == NULL)
        goto cleanup;

    // Walk up the tree.
    while (TRUE)
    {
        hr = pWalker->GetParentElement(pNode, &pParent);
        if (FAILED(hr) || pParent == NULL)
        {
            break;
        }
        g_pAutomation->CompareElements(pParent, pDesktop, &same);
        if (same)
        {
            pDesktop->Release();
            pParent->Release();
            pWalker->Release();
            // Reached desktop, so return next element below it.
            return pNode;
        }
        if (pNode != pChild) // Do not release the in-param.
            pNode->Release();
        pNode = pParent;
    }

cleanup:
    if ((pNode != NULL) && (pNode != pChild)) 
        pNode->Release();

    if (pDesktop != NULL)
        pDesktop->Release();

    if (pWalker != NULL)
        pWalker->Release();

    if (pParent != NULL)
        pParent->Release();

    return NULL;  
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Получение элементов автоматизации пользовательского интерфейса](uiauto-obtainingelements.md)
</dt> <dt>

[Разделы руководства по клиентам автоматизации пользовательского интерфейса](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




