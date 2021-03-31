---
title: Регистрация обратного вызова
description: Если приложению требуется уведомление при изменении значения переменной состояния или ее экземпляра службы, она становится недоступной, приложение должно зарегистрировать функцию обратного вызова.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9095ab4b5b2d43a12f7e806eabc24b174a0311
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792222"
---
# <a name="registering-a-callback"></a><span data-ttu-id="463be-103">Регистрация обратного вызова</span><span class="sxs-lookup"><span data-stu-id="463be-103">Registering a Callback</span></span>

<span data-ttu-id="463be-104">Если приложению требуется уведомление при изменении значения переменной состояния или ее экземпляра службы, она становится недоступной, приложение должно зарегистрировать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="463be-104">If the application requires notification when the value of a state variable changes or the service instance it represents becomes unavailable, the application must register a callback function.</span></span> <span data-ttu-id="463be-105">Чтобы зарегистрировать функцию обратного вызова для вызова объекта службы, используйте метод [**иупнпсервице:: аддкаллбакк**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="463be-105">To register a callback function for the service object to invoke, use the [**IUPnPService::AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="463be-106">Этот метод можно использовать для регистрации более одного обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="463be-106">This method can be used to register more than one callback.</span></span>

<span data-ttu-id="463be-107">Разработчики не должны отменять асинхронную операцию внутри асинхронного обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="463be-107">Developers should not cancel an asynchronous operation inside an asynchronous callback.</span></span>

> [!Note]  
> <span data-ttu-id="463be-108">Добавление обратного вызова в Visual Basic отличается от метода, используемого в VBScript.</span><span class="sxs-lookup"><span data-stu-id="463be-108">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="463be-109">Функция **GetRef** , используемая в VBScript, недоступна в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="463be-109">The **GetRef** function used in the VBScript is not available in Visual Basic.</span></span> <span data-ttu-id="463be-110">Поэтому разработчик должен создать объект [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , имеющий функцию обратного вызова в качестве метода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="463be-110">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="463be-111">См. раздел [Регистрация обратного вызова в Visual Basic](registering-a-callback-in-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="463be-111">See [Registering a Callback in Visual Basic](registering-a-callback-in-visual-basic.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="463be-112">Пример VBScript</span><span class="sxs-lookup"><span data-stu-id="463be-112">VBScript Example</span></span>

<span data-ttu-id="463be-113">Следующий код VBScript определяет функцию обратного вызова **сервицечанжекаллбакк**, которая вызывается, когда значения переменных состояния изменяются или когда экземпляр службы становится недоступным.</span><span class="sxs-lookup"><span data-stu-id="463be-113">The following VBScript code defines the callback function **serviceChangeCallback**, to be invoked when the values of state variables change or when the service instance becomes unavailable.</span></span> <span data-ttu-id="463be-114">Функция имеет четыре аргумента.</span><span class="sxs-lookup"><span data-stu-id="463be-114">The function has four arguments.</span></span>

<span data-ttu-id="463be-115">Первый аргумент функции указывает причину вызова обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="463be-115">The first argument to the function specifies the reason the callback is invoked.</span></span> <span data-ttu-id="463be-116">Он вызывается из-за изменения переменной состояния или недоступности экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="463be-116">It is invoked either because a state variable changed, or because the service instance has become unavailable.</span></span>

<span data-ttu-id="463be-117">Вторым аргументом является объект службы, для которого вызывается обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="463be-117">The second argument is the Service object for which the callback is invoked.</span></span> <span data-ttu-id="463be-118">Если для изменения переменной состояния вызывается обратный вызов, функция передается два дополнительных аргумента: имя изменяемой переменной и ее новое значение.</span><span class="sxs-lookup"><span data-stu-id="463be-118">If the callback is invoked for a state variable change, then the function is passed two additional arguments: the name of the variable that changed, and its new value.</span></span>

<span data-ttu-id="463be-119">В этом примере обратный вызов просто отображает окно сообщения, в котором отображается имя измененной переменной и ее новое значение, а также если обратный вызов был вызван для изменения переменной состояния.</span><span class="sxs-lookup"><span data-stu-id="463be-119">In this example, the callback simply displays a message box that shows the name of the changed variable and its new value, and if the callback was invoked for a state variable change.</span></span> <span data-ttu-id="463be-120">В противном случае отображается сообщение о том, что экземпляр службы больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="463be-120">Otherwise, it displays a message that indicates the service instance is no longer available.</span></span>

<span data-ttu-id="463be-121">В последней части фрагмента кода показано, как зарегистрировать функцию обратного вызова с помощью метода [**аддкаллбакк**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="463be-121">The last part of the code fragment shows how to register the callback function using the [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="463be-122">Предполагается, что переменные объекта службы, *appService* и *кспортсервице* , были инициализированы, как показано в [получении объектов службы](obtaining-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="463be-122">The service object variables, *appService* and *xportService* are assumed to have been initialized as shown in [Obtaining Service Objects](obtaining-service-objects.md).</span></span>


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



## <a name="c-example"></a><span data-ttu-id="463be-123">Пример C++</span><span class="sxs-lookup"><span data-stu-id="463be-123">C++ Example</span></span>


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



 

 