---
title: Поддержка шаблонов элементов управления в поставщике модели автоматизации пользовательского интерфейса
description: В этом разделе показано, как поставщик автоматизации пользовательского интерфейса Майкрософт реализует шаблоны элементов управления для элемента управления. Шаблоны элементов управления позволяют клиентским приложениям управлять элементом управления и получать сведения о нем.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649f9419c5e3003c0185f435cba4d38f4a25c3d7adc1bdc7cf9c53cd06b32a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759234"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a>Поддержка шаблонов элементов управления в поставщике модели автоматизации пользовательского интерфейса

В этом разделе показано, как поставщик автоматизации пользовательского интерфейса Майкрософт реализует шаблоны элементов управления для элемента управления. Шаблоны элементов управления позволяют клиентским приложениям управлять элементом управления и получать сведения о нем.

Поставщик реализует шаблон элемента управления, выполнив следующие основные действия.

1.  Реализуйте интерфейс поставщика, который поддерживает шаблон элемента управления. Например, для поддержки шаблона элемента управления [Selection](uiauto-implementingselection.md) поставщик для пользовательского элемента управления "список" будет реализовывать интерфейс [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .
2.  Возвращает объект, содержащий интерфейс поставщика шаблона элемента управления, когда модель автоматизации пользовательского интерфейса вызывает метод [**иравелементпровидерсимпле:: жетпаттернпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) поставщика.

В следующем примере показана реализация интерфейса [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) для пользовательского элемента управления списка с одним выбором. Реализация включает методы получения свойств для свойств Исселектионрекуиред и Канселектмултипле, а также метод для получения поставщика для выбранного элемента списка.


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



В следующем примере показана реализация [**иравелементпровидерсимпле:: жетпаттернпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) , которая возвращает объект, реализующий [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider). Большинство элементов управления "список" также поддерживают другие шаблоны, но в этом примере возвращается пустая ссылка для всех других идентификаторов шаблонов элементов управления.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Разделы руководства для поставщиков автоматизации пользовательского интерфейса](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




