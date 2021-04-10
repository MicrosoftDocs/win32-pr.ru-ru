---
title: Получение объектов службы
description: Объекты устройств предоставляют свойство, именуемое Services, которое возвращает коллекцию объектов службы, которая содержит один объект службы для каждой службы, экспортируемой устройством.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf951c9c620c23c2d4919dc4a8bcf082159fa7a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890920"
---
# <a name="obtaining-service-objects"></a>Получение объектов службы

Объекты устройств предоставляют свойство, именуемое [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) , которое возвращает коллекцию объектов службы, которая содержит один объект службы для каждой службы, экспортируемой устройством. Приложения могут последовательно просматривать эту коллекцию или запрашивать определенную службу с помощью ее идентификатора службы.

## <a name="vbscript-example"></a>Пример VBScript

Ниже приведен пример кода на языке VBScript, который извлекает объекты службы для двух служб, экспортируемых устройством.


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



Первая строка извлекает коллекцию служб из объекта Device, запрашивая свойство [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) . Следующие две строки получают два требуемых объекта службы из коллекции, указывая их идентификаторы служб. Коллекцию служб также можно просмотреть последовательно, используя **для каждой... Следующий** цикл.

## <a name="c-example"></a>Пример C++

В следующем примере показан код C++, необходимый для получения объектов службы с устройства. Во первых, пример кода запрашивает свойство [**иупнпдевице:: Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) интерфейса, переданного функции. Это возвращает коллекцию служб с помощью интерфейса [**иупнпсервицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) . Чтобы получить отдельные объекты службы, используйте метод [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) и укажите запрошенные идентификаторы служб. Для последовательного прохода по коллекции используйте методы [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)и [**IEnumVARIANT:: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) . Этот пример похож на пример, используемый для обхода коллекции [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")


HRESULT ExtractServices(IUPnPDevice * pDevice)
{
    // Create a BSTR to hold the service name
    BSTR bstrServiceName = SysAllocString(L"urn:upnp-org:servicId:DVDVideo");
    if (NULL == bstrServiceName)
    {
        return E_OUTOFMEMORY;
    }
    // Get the list of services available on the device
    IUPnPServices * pServices = NULL;
    HRESULT hr = pDevice->get_Services(&pServices);
    if (SUCCEEDED(hr))
    {
        // Retrieve the service we are interested in
        IUPnPService * pAppService = NULL;
        hr = pServices->get_Item(bstrServiceName, &pAppService);
        if (SUCCEEDED(hr))
        {
            // Do something interesting with the service object
            pAppService->Release();
        }
        pServices->Release();
    }
    SysFreeString(bstrServiceName);
    return hr;
}
```



 

 