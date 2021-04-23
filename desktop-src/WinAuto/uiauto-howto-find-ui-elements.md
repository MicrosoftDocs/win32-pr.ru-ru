---
title: Поиск элементов пользовательского интерфейса
description: В этом разделе содержится пример кода, в котором показано, как найти элементы пользовательского интерфейса в дереве модели автоматизации пользовательского интерфейса.
ms.assetid: b613eb18-e14d-468e-833d-072bad29ba06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887ef914d7abcf5ed6dfc546f0930334f53215d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531874"
---
# <a name="how-to-find-ui-elements"></a><span data-ttu-id="fab60-103">Поиск элементов пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fab60-103">How to Find UI Elements</span></span>

<span data-ttu-id="fab60-104">В этом разделе содержится пример кода, в котором показано, как найти элементы пользовательского интерфейса в дереве модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fab60-104">This topic contains example code that shows how to find a UI elements in the UI Automation tree.</span></span>

-   [<span data-ttu-id="fab60-105">Поиск элемента по имени</span><span class="sxs-lookup"><span data-stu-id="fab60-105">Finding an Element by Name</span></span>](#finding-an-element-by-name)
-   [<span data-ttu-id="fab60-106">Поиск связанных элементов</span><span class="sxs-lookup"><span data-stu-id="fab60-106">Finding Related Elements</span></span>](#finding-related-elements)
-   [<span data-ttu-id="fab60-107">См. также</span><span class="sxs-lookup"><span data-stu-id="fab60-107">Related topics</span></span>](#related-topics)

## <a name="finding-an-element-by-name"></a><span data-ttu-id="fab60-108">Поиск элемента по имени</span><span class="sxs-lookup"><span data-stu-id="fab60-108">Finding an Element by Name</span></span>

<span data-ttu-id="fab60-109">В следующем примере выполняется поиск элемента Microsoft UI Automation с указанным именем и является дочерним элементом окна рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="fab60-109">The following example finds the Microsoft UI Automation element that has the specified name and is a child of the desktop window.</span></span>


```C++
IUIAutomationElement* GetTopLevelWindowByName(LPWSTR windowName)
{
    if (windowName == NULL)
    {
        return NULL;
    }

    VARIANT varProp;
    varProp.vt = VT_BSTR;
    varProp.bstrVal = SysAllocString(windowName);
    if (varProp.bstrVal == NULL)
    {
        return NULL;
    }

    IUIAutomationElement* pRoot = NULL;
    IUIAutomationElement* pFound = NULL;

    // Get the desktop element. 
    HRESULT hr = g_pAutomation->GetRootElement(&pRoot);
    if (FAILED(hr) || pRoot == NULL)
        goto cleanup;

    // Get a top-level element by name, such as "Program Manager"
    IUIAutomationCondition* pCondition;
    hr = g_pAutomation->CreatePropertyCondition(UIA_NamePropertyId, varProp, &pCondition);
    if (FAILED(hr))
        goto cleanup;

    pRoot->FindFirst(TreeScope_Children, pCondition, &pFound);

cleanup:
    if (pRoot != NULL)
        pRoot->Release();

    if (pCondition != NULL)
        pCondition->Release();

    VariantClear(&varProp);
    return pFound;
}
```



## <a name="finding-related-elements"></a><span data-ttu-id="fab60-110">Поиск связанных элементов</span><span class="sxs-lookup"><span data-stu-id="fab60-110">Finding Related Elements</span></span>

<span data-ttu-id="fab60-111">Следующий пример функции возвращает коллекцию всех включенных кнопок, являющихся дочерними для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="fab60-111">The following example function returns a collection of all enabled buttons that are children of the specified element.</span></span>


```C++
IUIAutomationElementArray* GetEnabledButtons(IUIAutomationElement* pParent)
{
    if (pParent == NULL)
    {
        return NULL;
    }
    IUIAutomationCondition* pButtonCondition = NULL;
    IUIAutomationCondition* pEnabledCondition = NULL;
    IUIAutomationCondition* pCombinedCondition = NULL;
    IUIAutomationElementArray* pFound = NULL;

    // Create a property condition for the button control type.
    VARIANT varProp;
    varProp.vt = VT_I4;
    varProp.lVal = UIA_ButtonControlTypeId;
    g_pAutomation->CreatePropertyCondition(UIA_ControlTypePropertyId, varProp, &pButtonCondition);
    if (pButtonCondition == NULL)
        goto cleanup;

    // Create a property condition for the enabled property.
    varProp.vt = VT_BOOL;
    varProp.boolVal = VARIANT_TRUE;
    g_pAutomation->CreatePropertyCondition(UIA_IsEnabledPropertyId, varProp, &pEnabledCondition);
    if (pEnabledCondition == NULL)
        goto cleanup;

    // Combine the conditions.
    g_pAutomation->CreateAndCondition(pButtonCondition, pEnabledCondition, &pCombinedCondition);
    if (pCombinedCondition == NULL)
        goto cleanup;

    // Find the matching elements. Note that if the scope is changed to TreeScope_Descendants, 
    // system buttons on the caption bar will be found as well.
    pParent->FindAll(TreeScope_Children, pCombinedCondition, &pFound);

cleanup:
    if (pButtonCondition != NULL)
        pButtonCondition->Release();

    if (pEnabledCondition != NULL) 
        pEnabledCondition->Release();
    
    if (pCombinedCondition != NULL)
        pCombinedCondition->Release();

    return pFound;
}
```



## <a name="related-topics"></a><span data-ttu-id="fab60-112">См. также</span><span class="sxs-lookup"><span data-stu-id="fab60-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fab60-113">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="fab60-113">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fab60-114">Получение элементов автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fab60-114">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="fab60-115">Разделы руководства по клиентам автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fab60-115">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




