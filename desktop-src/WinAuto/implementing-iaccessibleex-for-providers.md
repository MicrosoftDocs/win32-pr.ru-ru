---
title: Реализация IAccessibleEx для поставщиков
description: В этом разделе объясняется, как добавить возможности поставщика автоматизации пользовательского интерфейса Майкрософт на сервер Microsoft Active Accessibility, реализовав интерфейс IAccessibleEx.
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710296"
---
# <a name="implementing-iaccessibleex-for-providers"></a>Реализация IAccessibleEx для поставщиков

В этом разделе объясняется, как добавить возможности поставщика автоматизации пользовательского интерфейса Майкрософт на сервер Microsoft Active Accessibility, реализовав интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Перед реализацией [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)учитывайте следующие требования.

-   Базовая иерархия объектов Microsoft Active Accessibility со специальными возможностями должна быть чистой. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) не может устранить проблемы с существующими иерархиями доступных объектов. Перед реализацией **IAccessibleEx** необходимо исправить все проблемы, связанные со структурой объектной модели, в реализации Microsoft Active Accessibility.
-   Реализация [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) должна соответствовать спецификации Microsoft Active Accessibility и спецификации автоматизации пользовательского интерфейса. Доступны средства для проверки соответствия в обеих спецификациях. Дополнительные сведения см. в разделе [средства тестирования](testing-tools.md) и [Автоматизация пользовательского интерфейса Проверка платформы автоматизации тестирования (UIA Verify)](https://www.codeplex.com/UIAutomationVerify/).

Для реализации [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) необходимо выполнить следующие основные действия.

-   Реализуйте **IServiceProvider** для доступного объекта, чтобы интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) можно было найти в этом или отдельном объекте.
-   Реализуйте [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для доступного объекта.
-   Создайте объекты со специальными возможностями для любых дочерних элементов Microsoft Active Accessibility, которые в Microsoft Active Accessibility представлены интерфейсом [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) родительского объекта (например, элементы списка). Реализуйте [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для этих объектов.
-   Реализуйте [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для всех доступных объектов.
-   Реализуйте соответствующие интерфейсы шаблона элемента управления в доступных объектах.

### <a name="implementing-the-iserviceprovider-interface"></a>Реализация интерфейса IServiceProvider

Поскольку реализация [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для элемента управления может находиться в отдельном объекте, клиентские приложения не могут использовать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения этого интерфейса. Вместо этого клиенты должны вызывать метод **IServiceProvider:: QueryService**. В следующем примере реализации этого метода предполагается, что **IAccessibleEx** не реализован в отдельном объекте. Поэтому метод просто вызывается через **QueryInterface**.


```C++
           
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_NOINTERFACE;
    }
};      
```



### <a name="implementing-the-iaccessibleex-interface"></a>Реализация интерфейса IAccessibleEx

В Microsoft Active Accessibility элемент пользовательского интерфейса всегда определяется интерфейсом [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и идентификатором дочернего элемента. Один экземпляр **IAccessible** может представлять несколько элементов пользовательского интерфейса.

Так как каждый экземпляр [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) представляет только один элемент пользовательского интерфейса, каждая пара идентификаторов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и Child должна быть сопоставлена с одним экземпляром **IAccessibleEx** . **IAccessibleEx** содержит два метода для решения этого сопоставления:

-   [**Жетобжектфорчилд**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)— получает интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для указанного дочернего элемента. Этот метод возвращает **значение NULL** , если реализация **IAccessibleEx** не распознает указанный идентификатор дочернего элемента, не имеет **IAccessibleEx** для указанного дочернего элемента или представляет дочерний элемент.
-   [**Жетиакцессиблепаир**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)— Извлекает интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и идентификатор потомка для элемента [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Для реализаций **IAccessible** , не использующих идентификатор дочернего элемента, этот метод извлекает соответствующий объект **IAccessible** и чилдид \_ себя.

В следующем примере показана реализация методов [**жетобжектфорчилд**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) и [**жетиакцессиблепаир**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) для элемента в пользовательском представлении списка. Методы позволяют модели автоматизации пользовательского интерфейса сопоставить пару ИДЕНТИФИКАТОРов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и Child с соответствующим экземпляром [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .


```C++
           
HRESULT CListboxAccessibleObject::GetObjectForChild(
    long idChild, IAccessibleEx **ppRetVal)
{ 
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;
    HRESULT hr = ValidateChildId(vChild);
    if (FAILED(hr))
    {
        return E_INVALIDARG;
    }
    // List item accessible objects are stored as an array of
    // pointers; for the purpose of this example it is assumed that 
    // the list contents will not change. Accessible objects are
    // created only when needed.
    if (itemProviders[idChild - 1] == NULL)
    {
        // Create an object that supports UI Automation and
        // IAccessibleEx for the item.
        itemProviders[idChild - 1] = 
          new CListItemAccessibleObject(idChild, 
          g_pListboxControl);
        if (itemProviders[idChild - 1] == NULL)
        {
            return E_OUTOFMEMORY;
        }
    }
    IAccessibleEx* pAccEx = static_cast<IAccessibleEx*>
      (itemProviders[idChild - 1]);
    if (pAccEx != NULL)
    {
      pAccEx->AddRef();
    }
    *ppRetVal = pAccEx;
    return S_OK; 
}

HRESULT CListItemAccessibleObject::GetIAccessiblePair(
    IAccessible **ppAcc, long *pidChild)
{ 
    if (ppAcc == NULL || pidChild == NULL)
    {
        return E_INVALIDARG;   
    }

                CListboxAccessibleObject* pParent = 
        m_control->GetAccessibleObject();

    HRESULT hr = pParent->QueryInterface( 
        __uuidof(IAccessible), (void**)ppAcc);
    if (FAILED(hr))
    {
        *pidChild = 0;
        return E_NOINTERFACE;
    }
    *pidChild = m_childID; 
    return S_OK; 
}
}
```



Если в реализации доступного объекта не используется идентификатор дочернего элемента, методы могут по-прежнему быть реализованы, как показано в следующем фрагменте кода.


```C++
           

    // This sample implements IAccessibleEx on the same object; it could use a tear-off
    // or inner object instead.
    class MyAccessibleImpl: public IAccessible,
                        public IAccessibleEx,
                        public IRawElementProviderSimple
    {
    public:
    ...
   HRESULT STDMETHODCALLTYPE GetObjectForChild( long idChild, IAccessibleEx **ppRetVal )
    {
        // This implementation does not support child IDs.
        *ppRetVal = NULL;
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE GetIAccessiblePair( IAccessible ** ppAcc, long * pidChild )
    {
        // This implementation assumes that IAccessibleEx is implemented on same object as
        // IAccessible.
        *ppAcc = static_cast<IAccessible *>(this);
        (*ppAcc)->AddRef();
        *pidChild = CHILDID_SELF;
        return S_OK;
    }
```



### <a name="implement-the-irawelementprovidersimple-interface"></a>Реализация интерфейса Иравелементпровидерсимпле

Серверы используют [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для предоставления сведений о свойствах и шаблонах элементов управления модели автоматизации пользовательского интерфейса. **Иравелементпровидерсимпле** включает следующие методы:

-   [**Жетпаттернпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)— этот метод используется для предоставления интерфейсов шаблонов элементов управления. Он возвращает объект, который поддерживает указанный шаблон элемента управления, или **значение NULL** , если шаблон элемента управления не поддерживается.
-   [**Жетпропертивалуе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)— этот метод используется для предоставления значений свойств модели автоматизации пользовательского интерфейса.
-   [**Хостравелементпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)— этот метод не используется с реализациями [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .
-   [**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)— этот метод не используется с реализациями [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Сервер [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) предоставляет шаблоны элементов управления, реализуя [**Иравелементпровидерсимпле:: жетпаттернпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). Этот метод принимает целочисленный параметр, указывающий шаблон элемента управления. Сервер возвращает **значение NULL** , если шаблон не поддерживается. Если интерфейс шаблона элемента управления поддерживается, серверы возвращают [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , а клиент вызывает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения соответствующего шаблона элемента управления.

Сервер [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) может поддерживать свойства модели автоматизации пользовательского интерфейса (например, Лабеледби и исрекуиредфорформ), реализуя [**Иравелементпровидерсимпле:: жетпропертивалуе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) и предоставляя целое число PROPERTYID, идентифицирующее свойство как параметр. Этот метод применим только к свойствам модели автоматизации пользовательского интерфейса, которые не включены в интерфейс шаблона элемента управления. Свойства, связанные с интерфейсом шаблона элемента управления, доступны через метод интерфейса шаблона элемента управления. Например, свойство со свойством, которое было выбрано из шаблона элемента управления [SelectionItem](uiauto-implementingselectionitem.md) , было бы предоставлено с помощью [**иселектионитемпровидер:: Get \_**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).

 

 