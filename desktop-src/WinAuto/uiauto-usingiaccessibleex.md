---
title: Добавление функций автоматизации пользовательского интерфейса на серверы Active Accessibility
description: Элементы управления, у которых нет поставщика Microsoft UI Automation, но реализующие IAccessible, можно легко обновить, чтобы обеспечить некоторые функции автоматизации пользовательского интерфейса, реализуя интерфейс IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Модель автоматизации пользовательского интерфейса, Active Accessibility серверы
- Модель автоматизации пользовательского интерфейса, серверы Microsoft Active Accessibility
- Модель автоматизации пользовательского интерфейса, IAccessible
- Модель автоматизации пользовательского интерфейса, IAccessibleEx
- Автоматизация пользовательского интерфейса, предоставление IAccessibleEx
- Модель автоматизации пользовательского интерфейса, реализация IAccessibleEx
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- предоставление IAccessibleEx
- Реализация IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb313205a69f6b69d07a377b006365837ee2a1410c51962000ea4ccff8b9037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823899"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a>Добавление функций автоматизации пользовательского интерфейса на серверы Active Accessibility

Элементы управления, у которых нет поставщика Microsoft UI Automation, но реализующие [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , можно легко обновить, чтобы обеспечить некоторые функции автоматизации пользовательского интерфейса, реализуя интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Этот интерфейс позволяет элементу управления предоставлять свойства автоматизации пользовательского интерфейса и шаблоны элементов управления без необходимости полной реализации интерфейсов поставщика автоматизации пользовательского интерфейса, таких как [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Чтобы реализовать **IAccessibleEx**, базовая иерархия объектов Microsoft Active Accessibility не должна содержать ошибок или несоответствий (например, дочернего объекта, родительский объект которого не является дочерним) и не должен конфликтовать со спецификациями модели автоматизации пользовательского интерфейса. Если иерархия объектов Microsoft Active Accessibility соответствует этим требованиям, это хороший кандидат на добавление функциональных возможностей с помощью **IAccessibleEx**; в противном случае необходимо реализовать автоматизацию пользовательского интерфейса отдельно или параллельно с реализацией Microsoft Active Accessibility.

Возьмем вариант пользовательского элемента управления, имеющего значение Range. Сервер Microsoft Active Accessibility для элемента управления определяет его роль и может возвращать его текущее значение, но не имеет средств для возврата минимального и максимального значений элемента управления, так как эти свойства не определены в Microsoft Active Accessibility. Клиент автоматизации пользовательского интерфейса может получить роль элемента управления, текущее значение и другие свойства Microsoft Active Accessibility, так как ядро автоматизации пользовательского интерфейса может получить их через [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Однако без доступа к интерфейсу [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) в объекте модель автоматизации пользовательского интерфейса также не может получить максимальное и минимальное значения.

Разработчик элемента управления может предоставить полный поставщик автоматизации пользовательского интерфейса для элемента управления, но это означает дублирование большинства существующих функциональных возможностей реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : например, навигации и общих свойств. Вместо этого разработчик может по-прежнему использовать **IAccessible** для предоставления этой функции, добавляя поддержку свойств конкретного элемента управления через [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

Для обновления пользовательского элемента управления требуются следующие основные шаги:

-   Реализуйте [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) для доступного объекта, чтобы интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) можно было найти в этом или отдельном объекте.
-   Реализуйте [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для доступного объекта.
-   Создавайте различные объекты со специальными возможностями для всех дочерних элементов Microsoft Active Accessibility, которые в Microsoft Active Accessibility могли быть представлены интерфейсом [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) родительского объекта (например, элементы списка). Реализуйте [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для этих объектов.
-   Реализуйте [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для всех доступных объектов.
-   Реализуйте соответствующие интерфейсы шаблона элемента управления в доступных объектах.

В этом разделе содержатся следующие подразделы.

-   [Предоставление IAccessibleEx](#exposing-iaccessibleex)
-   [Реализация IAccessibleEx](#implementing-iaccessibleex)
-   [Связанные темы](#related-topics)

## <a name="exposing-iaccessibleex"></a>Предоставление IAccessibleEx

Поскольку реализация [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для элемента управления может находиться в отдельном объекте, клиентские приложения не могут использовать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения этого интерфейса. Вместо этого клиенты должны вызывать метод [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)). В следующем примере реализации этого метода предполагается, что **IAccessibleEx** не реализован в отдельном объекте. Поэтому метод просто вызывается через **QueryInterface**.


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
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
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a>Реализация IAccessibleEx

Метод [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , который наиболее интересен, — это [**жетобжектфорчилд**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild). Этот метод дает серверу Microsoft Active Accessibility возможность создать доступный объект (который предоставляет, как минимум, **IAccessibleEx**) для дочернего элемента. В Microsoft Active Accessibility дочерние элементы обычно не представляются как объекты со специальными возможностями, но являются дочерними объектами доступного объекта. Однако, поскольку модель автоматизации пользовательского интерфейса требует, чтобы каждый элемент представлялся отдельным доступным объектом, **жетобжектфорчилд** должен создать отдельный объект для каждого дочернего элемента по запросу.

В следующем примере реализации возвращается доступный объект для элемента в пользовательском представлении списка.


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



Полный пример реализации см. в разделе [обеспечение доступности настраиваемых элементов управления, часть 5. Использование IAccessibleEx для добавления поддержки модели автоматизации пользовательского интерфейса в пользовательский элемент управления](/previous-versions/msdn10/cc307850(v=msdn.10)) в MSDN.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Рекомендации программиста поставщика модели автоматизации пользовательского интерфейса](uiauto-providerportal.md)
</dt> </dl>

 

 