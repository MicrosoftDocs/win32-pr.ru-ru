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
# <a name="obtaining-service-objects"></a><span data-ttu-id="faac6-103">Получение объектов службы</span><span class="sxs-lookup"><span data-stu-id="faac6-103">Obtaining Service Objects</span></span>

<span data-ttu-id="faac6-104">Объекты устройств предоставляют свойство, именуемое [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) , которое возвращает коллекцию объектов службы, которая содержит один объект службы для каждой службы, экспортируемой устройством.</span><span class="sxs-lookup"><span data-stu-id="faac6-104">Device objects expose a property called [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) that returns a collection of Service objects that contains one service object for each service exported by the device.</span></span> <span data-ttu-id="faac6-105">Приложения могут последовательно просматривать эту коллекцию или запрашивать определенную службу с помощью ее идентификатора службы.</span><span class="sxs-lookup"><span data-stu-id="faac6-105">Applications are able to traverse this collection sequentially, or request a particular service by using its service ID.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="faac6-106">Пример VBScript</span><span class="sxs-lookup"><span data-stu-id="faac6-106">VBScript Example</span></span>

<span data-ttu-id="faac6-107">Ниже приведен пример кода на языке VBScript, который извлекает объекты службы для двух служб, экспортируемых устройством.</span><span class="sxs-lookup"><span data-stu-id="faac6-107">The following example is VBScript code that extracts Service objects for two of the services exported by a device.</span></span>


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



<span data-ttu-id="faac6-108">Первая строка извлекает коллекцию служб из объекта Device, запрашивая свойство [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) .</span><span class="sxs-lookup"><span data-stu-id="faac6-108">The first line extracts the services collection from the Device object by querying the [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property.</span></span> <span data-ttu-id="faac6-109">Следующие две строки получают два требуемых объекта службы из коллекции, указывая их идентификаторы служб.</span><span class="sxs-lookup"><span data-stu-id="faac6-109">The next two lines obtain the two desired Service objects from the collection by specifying their service IDs.</span></span> <span data-ttu-id="faac6-110">Коллекцию служб также можно просмотреть последовательно, используя **для каждой... Следующий** цикл.</span><span class="sxs-lookup"><span data-stu-id="faac6-110">The services collection can also be traversed sequentially by using a **for each … next** loop.</span></span>

## <a name="c-example"></a><span data-ttu-id="faac6-111">Пример C++</span><span class="sxs-lookup"><span data-stu-id="faac6-111">C++ Example</span></span>

<span data-ttu-id="faac6-112">В следующем примере показан код C++, необходимый для получения объектов службы с устройства.</span><span class="sxs-lookup"><span data-stu-id="faac6-112">The following example shows the C++ code required to obtain Service objects from a device.</span></span> <span data-ttu-id="faac6-113">Во первых, пример кода запрашивает свойство [**иупнпдевице:: Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) интерфейса, переданного функции.</span><span class="sxs-lookup"><span data-stu-id="faac6-113">First, the sample code queries the [**IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property on the interface that was passed to the function.</span></span> <span data-ttu-id="faac6-114">Это возвращает коллекцию служб с помощью интерфейса [**иупнпсервицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) .</span><span class="sxs-lookup"><span data-stu-id="faac6-114">This returns a service collection using the [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) interface.</span></span> <span data-ttu-id="faac6-115">Чтобы получить отдельные объекты службы, используйте метод [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) и укажите запрошенные идентификаторы служб.</span><span class="sxs-lookup"><span data-stu-id="faac6-115">To obtain individual Service objects, use the [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) method, and specify the requested service IDs.</span></span> <span data-ttu-id="faac6-116">Для последовательного прохода по коллекции используйте методы [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)и [**IEnumVARIANT:: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) .</span><span class="sxs-lookup"><span data-stu-id="faac6-116">To traverse the collection sequentially, use the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next), and [**IEnumVARIANT::Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) methods.</span></span> <span data-ttu-id="faac6-117">Этот пример похож на пример, используемый для обхода коллекции [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="faac6-117">This example is similar to the example used to traverse the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) collection.</span></span>


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



 

 