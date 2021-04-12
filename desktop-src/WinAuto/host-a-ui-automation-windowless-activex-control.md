---
title: Размещение элемента управления ActiveX без окна модели автоматизации пользовательского интерфейса
description: Узнайте, как создать контейнер элементов управления, который может размещать элементы управления Microsoft ActiveX без окон, реализующие автоматизацию пользовательского интерфейса Майкрософт.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- Модель автоматизации пользовательского интерфейса, безоконный элемент управления ActiveX
- Безоконный элемент управления ActiveX, модель автоматизации пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337681"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a>Размещение элемента управления ActiveX без окна модели автоматизации пользовательского интерфейса

Узнайте, как создать контейнер элементов управления, который может размещать элементы управления Microsoft ActiveX без окон, реализующие автоматизацию пользовательского интерфейса Майкрософт. С помощью описанных здесь действий можно убедиться, что любые элементы управления без окон автоматизации пользовательского интерфейса, размещенные в контейнере управления, доступны для клиентских приложений с поддержкой специальных возможностей (AT).

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления ActiveX](/windows/desktop/com/activex-controls)
-   [Модель автоматизации пользовательского интерфейса](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование Microsoft Win32 и объектной модели компонентов (COM)
-   Элементы управления ActiveX без окон
-   Поставщики автоматизации пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a>Шаг 1. предоставление интерфейса Иравелементпровидерсимпле от имени элемента управления без окон.

Всякий раз, когда системе требуется указатель [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для корневого элемента управления без окон, система запрашивает контейнер элемента управления. Для получения указателя контейнер вызывает реализацию метода [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) элемента управления без окон.

Если контейнер элемента управления имеет реализацию модели автоматизации пользовательского интерфейса, он может вернуть в систему указатель [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) элемента управления без окон.

Если контейнер элемента управления имеет реализацию Microsoft Active Accessibility, вызовите функцию [**уиаиакцессиблефромпровидер**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) , чтобы получить указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , представляющий элемент управления, а затем верните указатель интерфейса **IAccessible** в систему.

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a>Шаг 2. Реализация интерфейса Иравелементпровидервиндовлесссите.

Контейнер элемента управления реализует интерфейс [**иравелементпровидервиндовлесссите**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) , позволяющий использовать безоконный элемент управления, основанный на модели автоматизации пользовательского интерфейса, для передачи сведений о специальных возможностях.

1.  Реализуйте [**иравелементпровидервиндовлесссите:: жетрунтимеидпрефикс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).

    Фрагмент управления без окон должен создать уникальный идентификатор среды выполнения. Чтобы создать идентификатор среды выполнения, фрагмент управления без окон извлекает значение префикса путем вызова метода [**жетрунтимеидпрефикс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) сайта элемента управления, а затем добавляет к префиксу целочисленное значение, уникальное относительно всех остальных фрагментов в безоконном элементе управления.

    Сайт управления для элемента управления без окон должен реализовывать метод [**жетрунтимеидпрефикс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) , формируя **массив SafeArray** , содержащий константу **уиааппендрунтимеид**, за которым следует целочисленное значение, уникальное для сайта.

    В этом примере показано, как вернуть префикс идентификатора среды выполнения для элемента управления без окон.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  Реализуйте метод [**иравелементпровидервиндовлесссите:: жетаджацентфрагмент**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .

    Элемент управления, реализующий автоматизацию пользовательского интерфейса, должен возвращать указатель на родительский поставщик фрагментов элемента управления.

    Чтобы получить родительский элемент фрагмента, объект, реализующий интерфейс [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) , должен иметь возможность реализовать метод [**navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) . Реализовать **навигацию** для безоконного элемента управления сложно, поскольку элемент управления может не определить его расположение в доступном дереве родительского объекта. Метод [**иравелементпровидервиндовлесссите:: жетаджацентфрагмент**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) позволяет безоконному элементу управления запрашивать его сайт для смежного фрагмента, а затем возвращать этот фрагмент клиенту, который вызвал команду **navigate**.

    В этом примере показано, как контейнер элемента управления Извлекает родительский фрагмент элемента управления без окон.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a>Шаг 3. необязательно. Реализация интерфейса Иравелементпровидерхостингакцессиблес.

Реализуйте интерфейс [**иравелементпровидерхостингакцессиблес**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) , если контейнер элемента управления имеет реализацию поставщика автоматизации пользовательского интерфейса, которая является корнем дерева специальных возможностей, включающего элементы управления ActiveX без окон, поддерживающие Microsoft Active Accessibility. Интерфейс **иравелементпровидерхостингакцессиблес** содержит один метод [**жетембеддедакцессиблес**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), который получает указатели интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) всех безоконных элементов управления ActiveX, работающих в Microsoft Active Accessibility, размещенных в контейнере элементов управления.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Размещение элемента управления ActiveX без окна MSAA](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[Специальные возможности элемента управления ActiveX без окон](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 