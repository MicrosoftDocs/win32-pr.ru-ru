---
title: Регистрация обратного вызова
description: Если приложению требуется уведомление при изменении значения переменной состояния или ее экземпляра службы, она становится недоступной, приложение должно зарегистрировать функцию обратного вызова.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3dca603e6226d3171aed920311bafcf6844ec9fab5c7aa05deafee7a13fd8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768534"
---
# <a name="registering-a-callback"></a>Регистрация обратного вызова

Если приложению требуется уведомление при изменении значения переменной состояния или ее экземпляра службы, она становится недоступной, приложение должно зарегистрировать функцию обратного вызова. Чтобы зарегистрировать функцию обратного вызова для вызова объекта службы, используйте метод [**иупнпсервице:: аддкаллбакк**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) . Этот метод можно использовать для регистрации более одного обратного вызова.

Разработчики не должны отменять асинхронную операцию внутри асинхронного обратного вызова.

> [!Note]  
> добавление обратного вызова в Visual Basic отличается от метода, используемого в VBScript. Функция **GetRef** , используемая в VBScript, недоступна в Visual Basic. Поэтому разработчик должен создать объект [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , имеющий функцию обратного вызова в качестве метода по умолчанию. См. раздел [Регистрация обратного вызова в Visual Basic](registering-a-callback-in-visual-basic.md).

 

## <a name="vbscript-example"></a>Пример VBScript

Следующий код VBScript определяет функцию обратного вызова **сервицечанжекаллбакк**, которая вызывается, когда значения переменных состояния изменяются или когда экземпляр службы становится недоступным. Функция имеет четыре аргумента.

Первый аргумент функции указывает причину вызова обратного вызова. Он вызывается из-за изменения переменной состояния или недоступности экземпляра службы.

Вторым аргументом является объект службы, для которого вызывается обратный вызов. Если для изменения переменной состояния вызывается обратный вызов, функция передается два дополнительных аргумента: имя изменяемой переменной и ее новое значение.

В этом примере обратный вызов просто отображает окно сообщения, в котором отображается имя измененной переменной и ее новое значение, а также если обратный вызов был вызван для изменения переменной состояния. В противном случае отображается сообщение о том, что экземпляр службы больше не доступен.

В последней части фрагмента кода показано, как зарегистрировать функцию обратного вызова с помощью метода [**аддкаллбакк**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) . Предполагается, что переменные объекта службы, *appService* и *кспортсервице* , были инициализированы, как показано в [получении объектов службы](obtaining-service-objects.md).


```VB
'State Change Callback Function
 
'Note:  In the sub declaration statement below, VARIABLE_UPDATE
'is one of two possible values for the callbackType argument; 
'the other is SERVICE_INSTANCE_DIED

Sub serviceChangeCallback(callbacktype, svcObj, varName, value)
    If (callbacktype = "VARIABLE_UPDATE") then
        Dim outString
        outString = "State Variable Changed:" & vbCrLf
        outString = outString & varName & " == " & value
    
        MsgBox(outString, "Service Callback")
    Else if (callbacktype = "SERVICE_INSTANCE_DIED") then
        MsgBox("Service instance is no longer available", 
               "Service Callback")
    End If
End Sub

' ...
    
'Add our state change callback to each service
appService.AddCallback GetRef("serviceChangeCallback")
xportService.AddCallback GetRef("serviceChangeCallback")
```



## <a name="c-example"></a>Пример C++


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

class CUPnPServiceCallback : public IUPnPServiceCallback
{
public:
    CUPnPServiceCallback()
    {
        m_lRefCount = 0;
    };
    
    STDMETHODIMP QueryInterface(REFIID iid, LPVOID* ppvObject)
    {
        HRESULT hr = S_OK;
        
        if(NULL == ppvObject)
        {
            hr = E_POINTER;
        }
        else
        {
            *ppvObject = NULL;
        }
        
        if(SUCCEEDED(hr))
        {
            if(IsEqualIID(iid, IID_IUnknown) || IsEqualIID(iid, IID_IUPnPServiceCallback))
            {
                *ppvObject = static_cast<IUPnPServiceCallback*>(this);
                AddRef();
            }
            else
            {
                hr = E_NOINTERFACE;
            }
        }
        
        return hr;
    };
    
    STDMETHODIMP_(ULONG) AddRef()
    {
        return ::InterlockedIncrement(&m_lRefCount);
    };
    
    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRefCount = ::InterlockedDecrement(&m_lRefCount);
        if(0 == lRefCount)
        {
            delete this;
        }
        
        return lRefCount;
    };
    
    STDMETHODIMP StateVariableChanged(IUPnPService *pus, LPCWSTR pcwszStateVarName, VARIANT varValue)
    {
        HRESULT    hr = S_OK;
        BSTR ServiceId;
        hr = pus->get_Id(&ServiceId);
        if (SUCCEEDED(hr))
        {
            VARIANT AlphaVariant;
            VariantInit(&AlphaVariant);
            hr = VariantChangeType(&AlphaVariant, &varValue, VARIANT_ALPHABOOL, VT_BSTR);
            if(SUCCEEDED(hr))
            {
                printf("StateVariableChanged called for the %S service"
                       " for %S state variable with the value=%S.\n",
                        ServiceId, pcwszStateVarName, V_BSTR(&AlphaVariant));
                VariantClear(&AlphaVariant);
            }
            SysFreeString(ServiceId);
        }
        return hr;
    };

    STDMETHODIMP ServiceInstanceDied(IUPnPService *pus)
    {
        HRESULT hr = S_OK;
        BSTR ServiceType;
        hr = pus->get_ServiceTypeIdentifier(&ServiceType);
        if(SUCCEEDED(hr))
        {
            printf("ServiceInstanceDied called for the %S service!\n", ServiceType);
            SysFreeString(ServiceType);
        }
        return hr;
    };
    
private:
    LONG m_lRefCount;
    
};

HRESULT AddCallbackToService(IUPnPService* pUPnPService)
{
    HRESULT hr = S_OK;

    IUnknown* pUPnPServiceCallback = new CUPnPServiceCallback;
    if(NULL != pUPnPServiceCallback)
    {
        pUPnPServiceCallback->AddRef();
        hr = pUPnPService->AddCallback(pUPnPServiceCallback);
        pUPnPServiceCallback->Release();
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
    return hr;
}
```



 

 