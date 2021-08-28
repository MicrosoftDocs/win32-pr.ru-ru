---
title: Получение виртуализированного элемента
description: В этом разделе содержится пример кода, который показывает, как найти и получить сведения о пользовательском интерфейсе виртуализированных элементов в элементе управления.
ms.assetid: 1882b8a9-0d03-4388-a1d0-1bff0ab9fc66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13a120d85ec106b05886128b4c5b44b81d377a933d4f8eb473500ba69aa9d17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859494"
---
# <a name="how-to-retrieve-a-virtualized-item"></a>Получение виртуализированного элемента

В этом разделе содержится пример кода, который показывает, как найти и получить сведения о пользовательском интерфейсе виртуализированных элементов в элементе управления.


В следующем примере выполняется поиск элемента с указанным именем в контейнере и получение интерфейса [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) для элемента. В примере сначала выполняется просмотр поддерева модели автоматизации пользовательского интерфейса. Если элемент отсутствует, в примере используется интерфейс [**иуиаутоматионитемконтаинерпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) контейнера для поиска элемента, а затем используется интерфейс Item [**иуиаутоматионвиртуализедитемпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) для реализации элемента.


```C++
HRESULT GetContainerItem (BSTR bstrItemName, IUIAutomationElement *pContainerElement, 
                          IUIAutomationElement **ppItemElement)                                  
{
    HRESULT hr;
    VARIANT varNameStr;
    IUIAutomationCondition *pNamePropertyCond = NULL;
    IUIAutomationElement *pFoundElement = NULL;
    IUIAutomationItemContainerPattern *pItemContainer = NULL;

    // Make sure the pointers are valid.
    if (ppItemElement == NULL || pContainerElement == NULL || bstrItemName == NULL)
        return E_INVALIDARG;
    
    *ppItemElement = NULL;

    // Try to find the item in the UI Automation tree. This attempt will fail if the
    // item is virtualized. Note: g_pAutomation is a global pointer to the IUIAutomation interface.
    varNameStr.vt = VT_BSTR;
    varNameStr.bstrVal = SysAllocString(bstrItemName);
    hr = g_pAutomation->CreatePropertyCondition(UIA_NamePropertyId, varNameStr, &pNamePropertyCond);
    if (pNamePropertyCond == NULL)
        goto cleanup;

    hr = pContainerElement->FindFirst(TreeScope_Subtree, pNamePropertyCond, &pFoundElement);
    if (pFoundElement == NULL) { 

        // The item is not in the UI Automation tree, so it may be virtualized. Try
        // using the ItemContainer control pattern to find the item.
        hr = pContainerElement->GetCurrentPatternAs(UIA_ItemContainerPatternId, 
                                                    __uuidof(IUIAutomationItemContainerPattern), 
                                                    (void**)&pItemContainer);
        if (pItemContainer == NULL)
            goto cleanup;

        hr = pItemContainer->FindItemByProperty(NULL, UIA_NamePropertyId, varNameStr, &pFoundElement);
        if (pFoundElement == NULL) // container has no item with the specified name
            goto cleanup;
    }

    // Attempt to get the name property. The attempt will fail with 
    // UIA_E_ELEMENTNOTAVAILABLE if the item is virtualized. 
    BSTR bstrName; 
    hr = pFoundElement->get_CurrentName(&bstrName);
    if (hr == UIA_E_ELEMENTNOTAVAILABLE) 
    {
        // The item might be virtualized. Use the VirtualizedItem control pattern to 
        // realize the item. 
        IUIAutomationVirtualizedItemPattern *pVirtualizedItem;
        hr = pFoundElement->GetCurrentPatternAs(UIA_VirtualizedItemPatternId, 
                    __uuidof(IUIAutomationVirtualizedItemPattern), (void**)&pVirtualizedItem);
        if (pVirtualizedItem == NULL)
            goto cleanup;

        hr = pVirtualizedItem->Realize();
        pVirtualizedItem->Release();

        if (hr != S_OK)
            goto cleanup;

        // Try to get the name again. 
        hr = pFoundElement->get_CurrentName(&bstrName);
    }    

    if (SUCCEEDED(hr))
    {
        // Make sure the item is the one we're looking for.
        if (wcscmp(bstrName, bstrItemName) == 0)
        {
            *ppItemElement = pFoundElement;
            pFoundElement = NULL;
        }
    }


cleanup:
        VariantClear(&varNameStr);

        if (pNamePropertyCond != NULL) pNamePropertyCond->Release();
        if (pFoundElement != NULL) pFoundElement->Release();
        if (pItemContainer != NULL) pItemContainer->Release();

        return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Работа с виртуализированными элементами](uiauto-workingwithvirtualizeditems.md)
</dt> <dt>

[Разделы руководства по клиентам автоматизации пользовательского интерфейса](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




