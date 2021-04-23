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
ms.openlocfilehash: 435a4552b364afbf909d04a759e3713ce69befab
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654359"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a><span data-ttu-id="28fe3-106">Поддержка сдвоенных или интерфейсов диспетчеризации</span><span class="sxs-lookup"><span data-stu-id="28fe3-106">Supporting Dual or Dispatch Interfaces</span></span>

<span data-ttu-id="28fe3-107">Как и интерфейс диспетчеризации, все сдвоенные интерфейсы должны наследовать от [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), который делегирует все свои функции **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**жеттипеинфокаунт**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) обратно в **IDispatch** агрегатора (ADSI).</span><span class="sxs-lookup"><span data-stu-id="28fe3-107">Like the dispatch interface, all dual interfaces must inherit from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), which delegates all of its **IDispatch** functions ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) back to the **IDispatch** of the aggregator (ADSI).</span></span> <span data-ttu-id="28fe3-108">Для делегирования объект расширения должен запрашивать интерфейс **IDispatch** агрегатора, вызывать соответствующий метод агрегации и освобождать указатель после использования.</span><span class="sxs-lookup"><span data-stu-id="28fe3-108">In order to delegate, an extension object should query for the **IDispatch** of the aggregator, call the appropriate aggregator method, and release the pointer after use.</span></span>

<span data-ttu-id="28fe3-109">Если расширение может быть отдельным компонентом, убедитесь, что оно является агрегатным.</span><span class="sxs-lookup"><span data-stu-id="28fe3-109">If the extension can be a standalone component, verify that it is aggregated.</span></span> <span data-ttu-id="28fe3-110">Если это так, передавайте функции диспетчеризации в [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) агрегата, в противном случае можно вызвать внутреннюю реализацию **IDispatch** или вызвать реализацию [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="28fe3-110">If so, reroute the dispatch functions to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) of the aggregator, otherwise you can call your internal implementation of **IDispatch**, or you can call your implementation of [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

<span data-ttu-id="28fe3-111">В следующем примере кода показано, как перенаправить вызов [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в **IDispatch** агрегата.</span><span class="sxs-lookup"><span data-stu-id="28fe3-111">The following code example shows how to reroute the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) call to the **IDispatch** of the aggregator.</span></span> <span data-ttu-id="28fe3-112">В этом примере кода предполагается, что переменная члена **m \_ паутерункновн** была инициализирована указателем **IUnknown** агрегатора.</span><span class="sxs-lookup"><span data-stu-id="28fe3-112">This code example assumes that the **m\_pOuterUnknown** member variable has been initialized to the **IUnknown** pointer of the aggregator.</span></span>


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



<span data-ttu-id="28fe3-113">Модули записи расширений настоятельно рекомендуется поддерживать сдвоенные интерфейсы вместо интерфейсов диспетчеризации в своих объектах расширения.</span><span class="sxs-lookup"><span data-stu-id="28fe3-113">Extension writers are strongly encouraged to support dual interfaces instead of dispatch interfaces in their extension objects.</span></span> <span data-ttu-id="28fe3-114">Сдвоенный интерфейс позволяет клиенту иметь более быстрый доступ при условии, что доступ к vtable включен в клиенте.</span><span class="sxs-lookup"><span data-stu-id="28fe3-114">A dual interface enables a client to have faster access, as long as vtable access is enabled in the client.</span></span> <span data-ttu-id="28fe3-115">Дополнительные сведения см. [в разделе позднее связывание и доступ к vtable в модели расширения ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span><span class="sxs-lookup"><span data-stu-id="28fe3-115">For more information, see [Late Binding vs. Vtable Access in the ADSI Extension Model](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span></span> <span data-ttu-id="28fe3-116">В зависимости от текущей модели реализация сдвоенных интерфейсов не должна быть сложнее, чем реализация интерфейсов диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="28fe3-116">Based on the current model, implementing dual interfaces should not be more difficult than implementing dispatch interfaces.</span></span>

 

 