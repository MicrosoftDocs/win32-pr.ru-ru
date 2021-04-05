---
title: Коллекции устройств, возвращенные синхронным поиском
description: Коллекции устройств — это объекты, содержащие один или несколько объектов устройств. Коллекция устройств предоставляет интерфейс Иупнпдевицес, предоставляющий методы и свойства для обхода коллекции и извлечения отдельных объектов устройств.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd581b7c79fe67a825e411d53e8c44c0f3d4326
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134286"
---
# <a name="device-collections-returned-by-synchronous-searches"></a>Коллекции устройств, возвращенные синхронным поиском

Коллекции устройств — это объекты, содержащие один или несколько объектов устройств. Коллекция устройств предоставляет интерфейс [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) , предоставляющий методы и свойства для обхода коллекции и извлечения отдельных объектов устройств.

## <a name="vbscript-example"></a>Пример VBScript

Приложения VBScript могут обращаться к объектам в коллекции двумя способами. Во-первых, они могут последовательно перемещаться по элементам с помощью for... каждый... Следующий цикл, как показано в следующем примере:


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



В этом примере предполагается, что переменная Devices была инициализирована в результате предыдущих условий поиска. Цикл выполняет шаги по объектам устройств в коллекции, назначая переменную Девицеобж значение каждого объекта устройства в свою очередь. Тело цикла может содержать код, обрабатывающий объект устройства.

## <a name="c-example"></a>Пример C++

В следующем примере показан код C++, необходимый для доступа к объектам в коллекции объектов устройств. Функция, показанная, **траверсеколлектион**, получает указатель на интерфейс [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) в качестве входного параметра. Этот указатель интерфейса может быть возвращен методом [**финдбитипе**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) или другими методами **Find** объекта Finder устройства.


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



Первым шагом является запрос нового перечислителя для коллекции с помощью свойства [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) . Он возвращает перечислитель в качестве интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Пример кода вызывает [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения интерфейса [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Затем пример кода устанавливает перечислитель в начало коллекции, вызывая метод [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) . Наконец, в примере кода вызывается метод [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) для прохода по коллекции. Объекты устройств в коллекции содержатся в структурах **Variant** . Эти структуры содержат указатели на интерфейсы [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в объектах устройств. Чтобы получить интерфейс [**иупнпдевице**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) , пример кода вызывает **QueryInterface** в интерфейсе **IDispatch** .

 

 