---
title: использование MSAA для обеспечения возможности управления ActiveX без окон
description: Описывает, как использовать Microsoft Active Accessibility \ 32; API, чтобы обеспечить доступность безоконного элемента управления Microsoft ActiveX для клиентских приложений с поддержкой специальных возможностей (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- ActiveX Элемент управления, Специальные возможности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bac5c4d2a27e5f069f2242999438eebe85e2ea7df1a6bc94890aec142db246c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098114"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>использование MSAA для обеспечения возможности управления ActiveX без окон

описывает, как использовать microsoft Active Accessibility API, чтобы гарантировать, что безоконный элемент управления microsoft ActiveX доступен для клиентских приложений с поддержкой специальных возможностей.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Элементы управления ActiveX](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Программирование Microsoft Win32 и объектной модели компонентов (COM)
-   безоконные элементы управления ActiveX
-   Серверы Microsoft Active Accessibility

## <a name="instructions"></a>Инструкции

### <a name="step-1-implement-the-iaccessible-interface"></a>Шаг 1. Реализация интерфейса IAccessible.

чтобы сделать безоконный контроль ActiveX доступным, необходимо реализовать интерфейс Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , точно так же, как и для элемента управления на основе окна, за исключением случаев, описанных в следующих шагах. Дополнительные сведения о реализации **IAccessible** см. в разделе " [рекомендации разработчика для Active Accessibility серверов](developer-s-guide-for-active-accessibility-servers.md)".

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Шаг 2. Реализация интерфейса IServiceProvider.

Когда клиент запрашивает сведения о специальных возможностях для безоконного управления, контейнер вызывает метод [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) элемента управления, чтобы получить указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

В этом примере показано, как реализовать метод [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>Шаг 3. Делегат IAccessible:: Get \_ аккпарент вызывает метод иакцессиблевиндовлесссите:: жетпарентакцессибле сайта элемента управления.

Когда клиент запрашивает родительский объект безоконного элемента управления, контейнер вызывает метод [**IAccessible:: Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) элемента управления. Реализация **Get \_ аккпарент** должна делегировать методу [**иакцессиблевиндовлесссите:: жетпарентакцессибле**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) контейнера.

В этом примере показано, как реализовать метод [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>Шаг 4. получение диапазона идентификаторов объектов для назначения источникам событий в безоконном управлении.

как и элементы управления на основе окон, ActiveX элемент управления без окон вызывает функцию [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) для уведомления клиентов о важных событиях. Параметры функции включают идентификатор объекта элемента, вызывающего событие. Элемент управления без окон должен назначать идентификаторы объектов с помощью значения из диапазона, полученного путем вызова метода [**иакцессиблевиндовлесссите:: аккуиреобжектидранже**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) сайта управления.

В этом примере показано, как получить диапазон значений идентификатора объекта из контейнера элемента управления.


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>Шаг 5. Реализация интерфейса Иакцессиблехандлер.

Когда безоконный элемент управления вызывает функцию [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , элемент управления указывает идентификатор объекта элемента пользовательского интерфейса, вызывающего событие, и указывает контейнер элемента управления как окно, которое будет реагировать на сообщения [**WM \_ GetObject**](wm-getobject.md) от имени элемента управления.

Если клиентское приложение отвечает на событие, контейнер элемента управления получает сообщение [**WM \_ GetObject**](wm-getobject.md) , включающее идентификатор объекта элемента пользовательского интерфейса, вызвавшего событие. Контейнер элемента управления отвечает путем поиска безоконного элемента управления, которому "владеет" идентификатор объекта, и последующего вызова метода [**иакцессиблехандлер:: акцессиблеобжектфромид**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) этого элемента управления. Метод **акцессиблеобжектфромид** возвращает указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента пользовательского интерфейса, а контейнер элементов управления перенаправляет указатель на клиентское приложение.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[используйте автоматизацию пользовательского интерфейса, чтобы сделать безоконный контроль ActiveX доступным](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[специальные возможности элемента управления ActiveX без окон](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 