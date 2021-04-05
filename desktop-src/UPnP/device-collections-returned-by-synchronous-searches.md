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
# <a name="device-collections-returned-by-synchronous-searches"></a><span data-ttu-id="60b2e-104">Коллекции устройств, возвращенные синхронным поиском</span><span class="sxs-lookup"><span data-stu-id="60b2e-104">Device Collections Returned By Synchronous Searches</span></span>

<span data-ttu-id="60b2e-105">Коллекции устройств — это объекты, содержащие один или несколько объектов устройств.</span><span class="sxs-lookup"><span data-stu-id="60b2e-105">Device collections are objects that contain one or more Device objects.</span></span> <span data-ttu-id="60b2e-106">Коллекция устройств предоставляет интерфейс [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) , предоставляющий методы и свойства для обхода коллекции и извлечения отдельных объектов устройств.</span><span class="sxs-lookup"><span data-stu-id="60b2e-106">A Device collection exposes the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface that provides methods and properties for traversing the collection and extracting individual device objects.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="60b2e-107">Пример VBScript</span><span class="sxs-lookup"><span data-stu-id="60b2e-107">VBScript Example</span></span>

<span data-ttu-id="60b2e-108">Приложения VBScript могут обращаться к объектам в коллекции двумя способами.</span><span class="sxs-lookup"><span data-stu-id="60b2e-108">VBScript applications can access the objects in the collection in two ways.</span></span> <span data-ttu-id="60b2e-109">Во-первых, они могут последовательно перемещаться по элементам с помощью for...</span><span class="sxs-lookup"><span data-stu-id="60b2e-109">First, they can traverse the elements sequentially using a for …</span></span> <span data-ttu-id="60b2e-110">каждый... Следующий цикл, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="60b2e-110">each ... next loop as shown in the following example:</span></span>


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



<span data-ttu-id="60b2e-111">В этом примере предполагается, что переменная Devices была инициализирована в результате предыдущих условий поиска.</span><span class="sxs-lookup"><span data-stu-id="60b2e-111">In this example, the devices variable is assumed to have been initialized with the result of a prior search.</span></span> <span data-ttu-id="60b2e-112">Цикл выполняет шаги по объектам устройств в коллекции, назначая переменную Девицеобж значение каждого объекта устройства в свою очередь.</span><span class="sxs-lookup"><span data-stu-id="60b2e-112">The loop steps through the Device objects in the collection, assigning the variable deviceObj the value of each Device object in turn.</span></span> <span data-ttu-id="60b2e-113">Тело цикла может содержать код, обрабатывающий объект устройства.</span><span class="sxs-lookup"><span data-stu-id="60b2e-113">The body of the loop can contain code that processes the Device object.</span></span>

## <a name="c-example"></a><span data-ttu-id="60b2e-114">Пример C++</span><span class="sxs-lookup"><span data-stu-id="60b2e-114">C++ Example</span></span>

<span data-ttu-id="60b2e-115">В следующем примере показан код C++, необходимый для доступа к объектам в коллекции объектов устройств.</span><span class="sxs-lookup"><span data-stu-id="60b2e-115">The following example shows the C++ code required to access the objects in a collection of device objects.</span></span> <span data-ttu-id="60b2e-116">Функция, показанная, **траверсеколлектион**, получает указатель на интерфейс [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="60b2e-116">The function shown, **TraverseCollection**, receives a pointer to the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface as an input parameter.</span></span> <span data-ttu-id="60b2e-117">Этот указатель интерфейса может быть возвращен методом [**финдбитипе**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) или другими методами **Find** объекта Finder устройства.</span><span class="sxs-lookup"><span data-stu-id="60b2e-117">This interface pointer could be returned by the [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method, or other **Find** methods, of the Device Finder object.</span></span>


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



<span data-ttu-id="60b2e-118">Первым шагом является запрос нового перечислителя для коллекции с помощью свойства [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="60b2e-118">The first step is to request a new enumerator for the collection using the [**\_NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) property.</span></span> <span data-ttu-id="60b2e-119">Он возвращает перечислитель в качестве интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="60b2e-119">This returns an enumerator as the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="60b2e-120">Пример кода вызывает [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения интерфейса [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="60b2e-120">The sample code invokes [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="60b2e-121">Затем пример кода устанавливает перечислитель в начало коллекции, вызывая метод [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) .</span><span class="sxs-lookup"><span data-stu-id="60b2e-121">The sample code then sets the enumerator to the beginning of the collection by invoking the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) method.</span></span> <span data-ttu-id="60b2e-122">Наконец, в примере кода вызывается метод [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) для прохода по коллекции.</span><span class="sxs-lookup"><span data-stu-id="60b2e-122">Finally, the sample code invokes the [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) method to traverse the collection.</span></span> <span data-ttu-id="60b2e-123">Объекты устройств в коллекции содержатся в структурах **Variant** .</span><span class="sxs-lookup"><span data-stu-id="60b2e-123">The device objects in the collection are contained within **VARIANT** structures.</span></span> <span data-ttu-id="60b2e-124">Эти структуры содержат указатели на интерфейсы [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в объектах устройств.</span><span class="sxs-lookup"><span data-stu-id="60b2e-124">These structures contain pointers to [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces on the device objects.</span></span> <span data-ttu-id="60b2e-125">Чтобы получить интерфейс [**иупнпдевице**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) , пример кода вызывает **QueryInterface** в интерфейсе **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="60b2e-125">To obtain the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface, the sample code invokes **QueryInterface** on the **IDispatch** interface.</span></span>

 

 