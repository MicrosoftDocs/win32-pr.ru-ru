---
description: Получение событий, поддерживаемых устройством
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Получение событий, поддерживаемых устройством
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547026"
---
# <a name="retrieving-the-events-supported-by-a-device"></a><span data-ttu-id="ed342-103">Получение событий, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="ed342-103">Retrieving the Events Supported by a Device</span></span>

<span data-ttu-id="ed342-104">Некоторые драйверы WPD поддерживают уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="ed342-104">Some WPD drivers support event notification.</span></span> <span data-ttu-id="ed342-105">Это означает, что приложение может зарегистрироваться в драйвере, чтобы получить уведомление при выполнении определенного действия.</span><span class="sxs-lookup"><span data-stu-id="ed342-105">This means that an application can register with the driver to receive a notification when a specific action occurs.</span></span> <span data-ttu-id="ed342-106">Например, приложение может зарегистрироваться, чтобы получить уведомление при добавлении или удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="ed342-106">For example, an application can register to receive a notification when an object is added or removed.</span></span>

<span data-ttu-id="ed342-107">Существует десять предопределенных событий, которые может отслеживать приложение.</span><span class="sxs-lookup"><span data-stu-id="ed342-107">There are ten predefined events that an application can monitor.</span></span> <span data-ttu-id="ed342-108">Они описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ed342-108">They are described in the following table.</span></span>



| <span data-ttu-id="ed342-109">Событие</span><span class="sxs-lookup"><span data-stu-id="ed342-109">Event</span></span>                       | <span data-ttu-id="ed342-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ed342-110">Description</span></span>                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed342-111">Возможности устройства обновлены</span><span class="sxs-lookup"><span data-stu-id="ed342-111">Device capabilities updated</span></span> | <span data-ttu-id="ed342-112">Происходит при изменении возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="ed342-112">Occurs when the device capabilities have changed.</span></span>                                                                                      |
| <span data-ttu-id="ed342-113">Устройство удалено</span><span class="sxs-lookup"><span data-stu-id="ed342-113">Device removed</span></span>              | <span data-ttu-id="ed342-114">Происходит при отсоединении устройства.</span><span class="sxs-lookup"><span data-stu-id="ed342-114">Occurs when the device is unplugged.</span></span>                                                                                                   |
| <span data-ttu-id="ed342-115">сброс настроек устройства;</span><span class="sxs-lookup"><span data-stu-id="ed342-115">Device reset</span></span>                | <span data-ttu-id="ed342-116">Происходит при сбросе устройства.</span><span class="sxs-lookup"><span data-stu-id="ed342-116">Occurs when the device has been reset.</span></span>                                                                                                 |
| <span data-ttu-id="ed342-117">Объект добавлен</span><span class="sxs-lookup"><span data-stu-id="ed342-117">Object added</span></span>                | <span data-ttu-id="ed342-118">Происходит после того, как новый объект станет доступным на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ed342-118">Occurs after a new object becomes available on the device.</span></span>                                                                             |
| <span data-ttu-id="ed342-119">Объект удален</span><span class="sxs-lookup"><span data-stu-id="ed342-119">Object removed</span></span>              | <span data-ttu-id="ed342-120">Происходит после удаления объекта с устройства.</span><span class="sxs-lookup"><span data-stu-id="ed342-120">Occurs after an object has been removed from the device.</span></span>                                                                               |
| <span data-ttu-id="ed342-121">Запрошено перемещение объектов</span><span class="sxs-lookup"><span data-stu-id="ed342-121">Object transfer requested</span></span>   | <span data-ttu-id="ed342-122">Указывает, что был выполнен запрос на перемещение объекта.</span><span class="sxs-lookup"><span data-stu-id="ed342-122">Indicates that a request has been made to transfer an object.</span></span>                                                                          |
| <span data-ttu-id="ed342-123">Объект обновлен</span><span class="sxs-lookup"><span data-stu-id="ed342-123">Object updated</span></span>              | <span data-ttu-id="ed342-124">Происходит после обновления объекта или его дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="ed342-124">Occurs after either an object or its children has been updated.</span></span> <span data-ttu-id="ed342-125">(Подключенные клиенты должны затем обновить представление заданного объекта.)</span><span class="sxs-lookup"><span data-stu-id="ed342-125">(Connected clients should then update their view of the given object.)</span></span> |
| <span data-ttu-id="ed342-126">Выполняется форматирование хранилища</span><span class="sxs-lookup"><span data-stu-id="ed342-126">Storage format in progress</span></span>  | <span data-ttu-id="ed342-127">Происходит при форматировании хранилища устройства.</span><span class="sxs-lookup"><span data-stu-id="ed342-127">Occurs when the device storage is being formatted.</span></span>                                                                                     |



 

<span data-ttu-id="ed342-128">Список констант, связанных с этими событиями, см. в разделе [константы событий](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="ed342-128">For a list of the constants associated with these events, see the [Event Constants](event-constants.md) topic.</span></span>

<span data-ttu-id="ed342-129">Функция Листсуппортедевентс в модуле Девицекапабилитиес. cpp демонстрирует получение событий, поддерживаемых данным устройством.</span><span class="sxs-lookup"><span data-stu-id="ed342-129">The ListSupportedEvents function in the DeviceCapabilities.cpp module demonstrates the retrieval of events supported by a given device.</span></span>

<span data-ttu-id="ed342-130">Приложение может извлекать идентификаторы для событий, поддерживаемых устройством, с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ed342-130">Your application can retrieve the identifiers for events supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="ed342-131">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ed342-131">Interface</span></span>                                                                                      | <span data-ttu-id="ed342-132">Описание</span><span class="sxs-lookup"><span data-stu-id="ed342-132">Description</span></span>                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="ed342-133">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ed342-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="ed342-134">Предоставляет доступ к методам получения поддерживаемых событий.</span><span class="sxs-lookup"><span data-stu-id="ed342-134">Provides access to the supported-event retrieval methods.</span></span> |
| [<span data-ttu-id="ed342-135">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="ed342-135">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="ed342-136">Используется для перечисления и хранения данных функциональной категории.</span><span class="sxs-lookup"><span data-stu-id="ed342-136">Used to enumerate and store functional-category data.</span></span>     |



 

<span data-ttu-id="ed342-137">Первая задача, выполняемая примером приложения, — это извлечение объекта [**ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , который используется для получения событий, поддерживаемых данным устройством.</span><span class="sxs-lookup"><span data-stu-id="ed342-137">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the events supported by the given device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="ed342-138">Поддерживаемые события извлекаются путем вызова метода [**ипортабледевицекапабилитиес:: жетсуппортедевентс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="ed342-138">The supported events are retrieved by calling the [**IPortableDeviceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="ed342-139">Этот метод получает коллекцию идентификаторов событий для данного устройства и сохраняет их в объекте [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , на который указывает аргумент певентс.</span><span class="sxs-lookup"><span data-stu-id="ed342-139">This method retrieves a collection of event identifiers for the given device and stores them in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object pointed to by the pEvents argument.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="ed342-140">Следующим шагом является получение количества поддерживаемых событий, чтобы приложение может выполнить итерацию по объекту [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) и получить идентификатор для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="ed342-140">The next step is to retrieve the count of supported events so that the application can iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object and retrieve the identifier for each.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="ed342-141">См. также</span><span class="sxs-lookup"><span data-stu-id="ed342-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed342-142">**Константы событий**</span><span class="sxs-lookup"><span data-stu-id="ed342-142">**Event Constants**</span></span>](event-constants.md)
</dt> <dt>

[<span data-ttu-id="ed342-143">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="ed342-143">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="ed342-144">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ed342-144">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="ed342-145">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="ed342-145">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="ed342-146">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="ed342-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



