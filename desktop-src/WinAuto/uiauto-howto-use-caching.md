---
title: Использование кэширования
description: В этом разделе содержится пример кода, демонстрирующий использование возможностей кэширования (или выборки) в дереве Microsoft UI Automation.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758621a8499202b820a6ffc3459fade57c2a485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710067"
---
# <a name="how-to-use-caching"></a>Использование кэширования

В этом разделе содержится пример кода, демонстрирующий использование возможностей кэширования (или выборки) в дереве Microsoft UI Automation. В нем рассматриваются следующие темы:

-   [Получение свойств и шаблонов элементов управления в кэше](#fetching-properties-and-control-patterns-into-the-cache)
-   [Получение свойств и шаблонов элементов управления из кэша](#retrieving-properties-and-control-patterns-from-the-cache)
-   [См. также](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a>Получение свойств и шаблонов элементов управления в кэше

В следующем примере кода показана функция, которая получает элементы из элемента управления "список" и кэширует шаблон элемента управления SelectionItem и свойство Name для каждого элемента. По умолчанию элементы списка возвращаются с полной ссылкой, чтобы все текущие свойства по-прежнему были доступны.


```C++
// Given a list element, caches a control pattern and a property for
// all the list items.
IUIAutomationElementArray* FindAndCacheListItems(IUIAutomationElement* pList)
{
    if (pList == NULL)
        return NULL;
    
    IUIAutomationCondition* pCondition = NULL;
    IUIAutomationCacheRequest* pCacheRequest = NULL;
    IUIAutomationElementArray* pFound = NULL;

    HRESULT hr = g_pAutomation->CreateTrueCondition(&pCondition);
    if (FAILED(hr))
        goto cleanup;

    hr = g_pAutomation->CreateCacheRequest(&pCacheRequest);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddPattern(UIA_SelectionItemPatternId);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddProperty(UIA_NamePropertyId);
    if (FAILED(hr))
        goto cleanup;

    pList->FindAllBuildCache(TreeScope_Children, pCondition, pCacheRequest, &pFound);
    
cleanup:
    if (pCondition != NULL)
        pCondition->Release();

    if (pCacheRequest != NULL)
        pCacheRequest->Release();

    return pFound;
}
```



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a>Получение свойств и шаблонов элементов управления из кэша

В следующем коде показано, как извлечь свойства и шаблоны элементов управления из кэша. Он извлекает шаблон элемента управления SelectionItem и свойство Name для элемента списка.


```C++
// Demonstrates retrieval of cached properties from a list item
// obtained in FindAndCacheListItems.
HRESULT GetCachedListItem(IUIAutomationElement* pItem)
{           
    if (pItem == NULL)
    {
        return E_INVALIDARG;
    }

    IUIAutomationSelectionItemPattern* pSelectionItemPattern;
    HRESULT hr = pItem->GetCachedPatternAs(UIA_SelectionItemPatternId, 
        IID_IUIAutomationSelectionItemPattern, (void**)&pSelectionItemPattern);
    if (pSelectionItemPattern != NULL)
    {
        // ... To do: Do something with the pattern.

        pSelectionItemPattern->Release();
    }

    // Retrieve a cached property.
    BSTR bstrName;
    hr = pItem->get_CachedName(&bstrName);
    if (SUCCEEDED(hr))
    {
        // ... To do: Do something with the property.

        // Clean up when done with name.
        SysFreeString(bstrName);
        bstrName = NULL;
    }

    BOOL isControl;

    // The following returns E_INVALIDARG because the property was not cached.
    // hr = pItem->get_CachedIsControlElement(&isControl);

    // The following is valid because we have a full reference to the object, therefore
    // we can get current properties. If the cache request had been made with 
    // AutomationElementMode_None, no current properties would be available from
    // this IUIAutomationElement.
    hr = pItem->get_CurrentIsControlElement(&isControl);
    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Кэширование свойств и шаблонов элементов управления автоматизации пользовательского интерфейса](uiauto-cachingforclients.md)
</dt> <dt>

[Разделы руководства по клиентам автоматизации пользовательского интерфейса](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




