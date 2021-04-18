---
description: Вызов методов службы
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Вызов методов службы
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b568ea169d0f3c6465d9879eb9eb01c0b46b526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712489"
---
# <a name="invoking-service-methods"></a><span data-ttu-id="136b6-103">Вызов методов службы</span><span class="sxs-lookup"><span data-stu-id="136b6-103">Invoking Service Methods</span></span>

<span data-ttu-id="136b6-104">Приложение Впдсервицесаписампле содержит код, демонстрирующий синхронное выполнение приложением методов, поддерживаемых данной службой контактов.</span><span class="sxs-lookup"><span data-stu-id="136b6-104">The WpdServicesApiSample application includes code that demonstrates how an application can invoke the methods supported by a given Contacts service synchronously..</span></span> <span data-ttu-id="136b6-105">В этом образце используются следующие интерфейсы</span><span class="sxs-lookup"><span data-stu-id="136b6-105">This sample uses the following interfaces</span></span>



|                                                                        |                                                                                                                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="136b6-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="136b6-106">Interface</span></span>                                                              | <span data-ttu-id="136b6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="136b6-107">Description</span></span>                                                                                                                                                             |
| [<span data-ttu-id="136b6-108">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="136b6-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="136b6-109">Используется для получения интерфейса **ипортабледевицесервицемесодс** для вызова методов в заданной службе.</span><span class="sxs-lookup"><span data-stu-id="136b6-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="136b6-110">**ипортабледевицесервицемесодс**</span><span class="sxs-lookup"><span data-stu-id="136b6-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | <span data-ttu-id="136b6-111">Используется для вызова метода службы.</span><span class="sxs-lookup"><span data-stu-id="136b6-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="136b6-112">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="136b6-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="136b6-113">Используется для хранения параметров исходящего метода и результатов входящего метода.</span><span class="sxs-lookup"><span data-stu-id="136b6-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="136b6-114">Может иметь **значение NULL** , если метод не требует никаких параметров или не возвращает никаких результатов.</span><span class="sxs-lookup"><span data-stu-id="136b6-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |



 

<span data-ttu-id="136b6-115">Когда пользователь выбирает параметр "9" в командной строке, приложение вызывает метод **инвокемесодс** , который находится в модуле сервицемесодс. cpp.</span><span class="sxs-lookup"><span data-stu-id="136b6-115">When the user chooses option "9" at the command line, the application invokes the **InvokeMethods** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="136b6-116">Обратите внимание, что до вызова методов пример приложения открывает службу контактов на подключенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="136b6-116">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="136b6-117">Методы службы инкапсулируют функциональные возможности, определяемые и реализуемые каждой службой.</span><span class="sxs-lookup"><span data-stu-id="136b6-117">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="136b6-118">Они уникальны для каждого типа службы и представлены идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="136b6-118">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="136b6-119">Например, служба Contacts определяет метод **бегинсинк** , который вызывается приложениями для подготовки устройства к синхронизации объектов Contact, и метод **ендсинк** для уведомления устройства о завершении синхронизации.</span><span class="sxs-lookup"><span data-stu-id="136b6-119">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="136b6-120">Приложения выполняют метод путем вызова [**ипортабледевицесервицемесодс:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="136b6-120">Applications execute a method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="136b6-121">Методы службы не следует путать с командами WPD.</span><span class="sxs-lookup"><span data-stu-id="136b6-121">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="136b6-122">Команды WPD являются частью стандартного интерфейса драйвера устройства WPD (DDI) и являются механизмом обмена данными между приложением WPD и драйвером.</span><span class="sxs-lookup"><span data-stu-id="136b6-122">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="136b6-123">Команды являются предопределенными, сгруппированные по категориям, **например \_ категории WPD \_ Common**, и представляются структурой **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="136b6-123">Commands are predefined, grouped by categories, for example, **WPD\_CATEGORY\_COMMON**, and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="136b6-124">Приложение отправляет команды драйверу устройства, вызывая [**ипортабледевицесервице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="136b6-124">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="136b6-125">Дополнительные сведения см. в разделе команды.</span><span class="sxs-lookup"><span data-stu-id="136b6-125">For more information, see the Commands topic.</span></span>

<span data-ttu-id="136b6-126">Метод **инвокемесодс** вызывает метод [**Ипортабледевицесервице:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="136b6-126">The **InvokeMethods** method invokes the [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="136b6-127">С помощью этого интерфейса он вызывает методы **бегинсинк** и **ендсинк** , вызывая метод [**ипортабледевицесервицемесодс:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) .</span><span class="sxs-lookup"><span data-stu-id="136b6-127">Using this interface, it invokes the **BeginSync** and **EndSync** methods by calling the [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="136b6-128">При каждом вызове **Invoke** приложение предоставляет рефгуид для вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="136b6-128">Each time it calls **Invoke**, the application supplies the REFGUID for the method that is invoked.</span></span>

<span data-ttu-id="136b6-129">В следующем коде используется метод **инвокемесодс** .</span><span class="sxs-lookup"><span data-stu-id="136b6-129">The following code uses the **InvokeMethods** method.</span></span>


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="136b6-130">См. также</span><span class="sxs-lookup"><span data-stu-id="136b6-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="136b6-131">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="136b6-131">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="136b6-132">**ипортабледевицесервицемесодс**</span><span class="sxs-lookup"><span data-stu-id="136b6-132">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="136b6-133">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="136b6-133">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



