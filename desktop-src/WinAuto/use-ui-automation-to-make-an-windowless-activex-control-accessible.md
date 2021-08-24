---
title: использование модели автоматизации пользовательского интерфейса для обеспечения доступа к безоконному ActiveX управления
description: Описывает, как использовать автоматизацию пользовательского интерфейса Майкрософт \ 32; API, чтобы обеспечить доступность безоконного элемента управления Microsoft ActiveX для клиентских приложений с поддержкой специальных возможностей (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- безоконный контроль ActiveX, специальные возможности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ef56d5f3a06bbfa21502c791163f2251506a10fda7da9d07ee04941ad39de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570364"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a>использование модели автоматизации пользовательского интерфейса для обеспечения доступа к безоконному ActiveX управления

описывает, как использовать API microsoft UI Automation, чтобы убедиться, что безоконный элемент управления microsoft ActiveX доступен для клиентских приложений с поддержкой специальных технологий (AT).

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Элементы управления ActiveX](/windows/desktop/com/activex-controls)
-   [Модель автоматизации пользовательского интерфейса](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Программирование Microsoft Win32 и объектной модели компонентов (COM)
-   безоконные элементы управления ActiveX
-   Поставщики автоматизации пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a>Шаг 1. Реализация интерфейсов поставщика автоматизации пользовательского интерфейса.

чтобы сделать приложение доступным, необходимо реализовать интерфейсы поставщика автоматизации пользовательского интерфейса для безоконного ActiveX управления, включая [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**иравелементпровидерфрагментрут**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)и [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents). Эти интерфейсы следует реализовать так же, как для элемента управления на основе окна, за исключением описанных ниже действий. Дополнительные сведения о реализации интерфейсов поставщика UIA см. в разделе [Справочник программиста поставщика автоматизации пользовательского интерфейса](uiauto-providerportal.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Шаг 2. Реализация интерфейса IServiceProvider.

Когда клиенту требуются сведения о специальных возможностях элемента управления без окон, контейнер элементов управления вызывает метод **IServiceProvider:: QueryService** элемента управления, чтобы получить указатель интерфейса [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для элемента управления.

В следующем примере показано, как реализовать метод **QueryService** .


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a>Шаг 3. Реализация метода Иравелементпровидерфрагмент:: Navigate.

При вызове метода [**иравелементпровидерфрагмент:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) элемента управления без окон для перехода к родительскому поставщику элемента управления без окон метод **navigate** должен делегировать методу [**иравелементпровидервиндовлесссите:: жетаджацентфрагмент**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) контейнера элемента управления.

В следующем примере показано, как реализовать метод [**navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a>Шаг 4. Реализация метода Иравелементпровидерфрагмент:: Жетрунтимеид.

Когда безоконный элемент управления получает вызов своего метода [**иравелементпровидерфрагмент:: жетрунтимеид**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) , элемент управления должен выполнить следующие действия:

1.  Получите префикс идентификатора среды выполнения, вызвав метод [**иравелементпровидервиндовлесссите:: жетрунтимеидпрефикс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) сайта управления.
2.  Создайте уникальный идентификатор среды выполнения для элемента управления, добавив целое число в префикс идентификатора среды выполнения.
3.  Верните идентификатор среды выполнения вызывающему объекту.

В следующем примере показано, как реализовать метод [**жетрунтимеид**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) .


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[использование MSAA для обеспечения возможности управления ActiveX без окон](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[специальные возможности элемента управления ActiveX без окон](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 