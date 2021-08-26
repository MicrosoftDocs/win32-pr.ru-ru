---
title: Поддержка сдвоенных или интерфейсов диспетчеризации
description: Как и интерфейс диспетчеризации, все сдвоенные интерфейсы должны наследовать от IDispatch, который делегирует все свои функции IDispatch (GetIDsOfNames, Invoke, GetTypeInfo, Жеттипеинфокаунт) обратно в IDispatch агрегатора (ADSI).
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- Поддержка сдвоенных или интерфейсов диспетчеризации ADSI
- расширения ADSI, Dual или Dispatch Interface
- ADSI ADSI, пример кода C/C++, делегирование методов IDispatch в агрегатор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b783e9448926d6d29a27e5fb0db519175f82a9af1935e9f13655db743a946bcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930015"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a>Поддержка сдвоенных или интерфейсов диспетчеризации

Как и интерфейс диспетчеризации, все сдвоенные интерфейсы должны наследовать от [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), который делегирует все свои функции **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**жеттипеинфокаунт**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) обратно в **IDispatch** агрегатора (ADSI). Для делегирования объект расширения должен запрашивать интерфейс **IDispatch** агрегатора, вызывать соответствующий метод агрегации и освобождать указатель после использования.

Если расширение может быть отдельным компонентом, убедитесь, что оно является агрегатным. Если это так, передавайте функции диспетчеризации в [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) агрегата, в противном случае можно вызвать внутреннюю реализацию **IDispatch** или вызвать реализацию [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension).

В следующем примере кода показано, как перенаправить вызов [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в **IDispatch** агрегата. В этом примере кода предполагается, что переменная члена **m \_ паутерункновн** была инициализирована указателем **IUnknown** агрегатора.


```C++
/////////////////////////////////////////////////// 
// Delegating IDispatch Methods to the aggregator
///////////////////////////////////////////////////
STDMETHODIMP MyExtension::GetTypeInfoCount(UINT* pctinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfoCount( pctinfo );
        pDisp->Release();
    }
    return hr;
}
 
 
STDMETHODIMP MyExtension::GetTypeInfo(UINT itinfo, LCID lcid, ITypeInfo** pptinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfo( itinfo, lcid, pptinfo );
        pDisp->Release();
    }
    
    return hr;
}
 
STDMETHODIMP MyExtension::GetIDsOfNames(REFIID riid, LPOLESTR* rgszNames, UINT cNames, LCID lcid, DISPID* rgdispid)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetIDsOfNames( riid, rgszNames, cNames, lcid, 
                 rgdispid);
        pDisp->Release();
    }
    
    return hr;
 
}
 
STDMETHODIMP MyExtension::Invoke(DISPID dispidMember, REFIID riid,
        LCID lcid, WORD wFlags, DISPPARAMS* pdispparams, VARIANT* 
                pvarResult, EXCEPINFO* pexcepinfo, UINT* puArgErr)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->Invoke( dispidMember, riid, lcid, wFlags, 
                 pdispparams, pvarResult, pexcepinfo, puArgErr);
        pDisp->Release();
    }
    
    return hr;
}
```



Модули записи расширений настоятельно рекомендуется поддерживать сдвоенные интерфейсы вместо интерфейсов диспетчеризации в своих объектах расширения. Сдвоенный интерфейс позволяет клиенту иметь более быстрый доступ при условии, что доступ к vtable включен в клиенте. Дополнительные сведения см. [в разделе позднее связывание и доступ к vtable в модели расширения ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md). В зависимости от текущей модели реализация сдвоенных интерфейсов не должна быть сложнее, чем реализация интерфейсов диспетчеризации.

 

 