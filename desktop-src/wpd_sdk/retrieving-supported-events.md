---
description: Получение поддерживаемых событий службы
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Получение поддерживаемых событий службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515b65b8ed062c346777224a64539f5229a704a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712682"
---
# <a name="retrieving-supported-service-events"></a><span data-ttu-id="03e18-103">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="03e18-103">Retrieving Supported Service Events</span></span>

<span data-ttu-id="03e18-104">Приложение Впдсервицесаписампле содержит код, демонстрирующий, как приложение может извлекать события, поддерживаемые данной службой контактов, вызывая методы для следующих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="03e18-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the events supported by a given Contacts service by calling methods on the following interfaces.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03e18-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="03e18-105">Interface</span></span>                                                                            | <span data-ttu-id="03e18-106">Описание</span><span class="sxs-lookup"><span data-stu-id="03e18-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="03e18-107">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="03e18-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="03e18-108">Используется для получения интерфейса **ипортабледевицесервицекапабилитиес** для доступа к поддерживаемым событиям.</span><span class="sxs-lookup"><span data-stu-id="03e18-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="03e18-109">**ипортабледевицесервицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="03e18-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="03e18-110">Предоставляет доступ к поддерживаемым событиям и атрибутам событий.</span><span class="sxs-lookup"><span data-stu-id="03e18-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="03e18-111">**ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="03e18-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="03e18-112">Содержит список поддерживаемых событий.</span><span class="sxs-lookup"><span data-stu-id="03e18-112">Contains the list of supported events.</span></span>                                                                |
| [<span data-ttu-id="03e18-113">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="03e18-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="03e18-114">Содержит атрибуты для данного события.</span><span class="sxs-lookup"><span data-stu-id="03e18-114">Contains the attributes for a given event.</span></span>                                                            |



 

<span data-ttu-id="03e18-115">Когда пользователь выбирает параметр "4" в командной строке, приложение вызывает метод **листсуппортедевентс** , который находится в модуле сервицекапабилитиес. cpp.</span><span class="sxs-lookup"><span data-stu-id="03e18-115">When the user chooses option "4" at the command line, the application invokes the **ListSupportedEvents** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="03e18-116">Обратите внимание, что перед получением списка событий пример приложения открывает службу контактов на подключенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="03e18-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="03e18-117">В WPD событие описывается по имени, параметрам и параметрам.</span><span class="sxs-lookup"><span data-stu-id="03e18-117">In WPD, an event is described by its name, options, and parameters.</span></span> <span data-ttu-id="03e18-118">Имя события является строкой, понятной для сценария, например "Микустомевент".</span><span class="sxs-lookup"><span data-stu-id="03e18-118">The event name is a script-friendly string, for example, "MyCustomEvent".</span></span> <span data-ttu-id="03e18-119">Параметры события указывают, будет ли заданное событие пересылаться всем клиентам и поддерживает ли это событие автозапуск.</span><span class="sxs-lookup"><span data-stu-id="03e18-119">The event options indicate whether a given event is broadcast to all clients and whether that event supports autoplay.</span></span> <span data-ttu-id="03e18-120">Атрибуты параметра события включают PROPERTYKEY и VARTYPE данного параметра.</span><span class="sxs-lookup"><span data-stu-id="03e18-120">The event parameter attributes includes a given parameter's PROPERTYKEY and VARTYPE.</span></span>

<span data-ttu-id="03e18-121">Четыре метода в модуле Сервицекапабилитиес. cpp поддерживают получение поддерживаемых событий для данной службы Contacts: **листсуппортедевентс**, **дисплайевент**, **дисплайевентоптионс** и **дисплайевентпараметерс**.</span><span class="sxs-lookup"><span data-stu-id="03e18-121">Four methods in the ServiceCapabilities.cpp module support the retrieval of supported events for the given Contacts service: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions**, and **DisplayEventParameters**.</span></span> <span data-ttu-id="03e18-122">Метод **листсуппортедевентс** извлекает количество поддерживаемых событий и идентификатор GUID для каждого события.</span><span class="sxs-lookup"><span data-stu-id="03e18-122">The **ListSupportedEvents** method retrieves a count of supported events and the GUID identifier for each event.</span></span> <span data-ttu-id="03e18-123">Метод **дисплайевент** отображает имя события или идентификатор GUID, а затем вызывает **дисплайевентоптионс** и **дисплайевентпараметерс** для отображения данных, связанных с событиями.</span><span class="sxs-lookup"><span data-stu-id="03e18-123">The **DisplayEvent** method displays the event name or GUID, and then calls **DisplayEventOptions** and **DisplayEventParameters** to display the event-related data.</span></span>

<span data-ttu-id="03e18-124">Метод **листсуппортедевентс** вызывает метод [**Ипортабледевицесервице:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="03e18-124">The **ListSupportedEvents** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="03e18-125">Используя этот интерфейс, он получает поддерживаемые события, вызывая метод [**ипортабледевицесервицекапабилитиес:: жетсуппортедевентс**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="03e18-125">Using this interface, it retrieves the supported events by calling the [**IPortableDeviceServiceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="03e18-126">Метод **жетсуппортедевентс** извлекает идентификаторы GUID для каждого события, поддерживаемого службой, и КОПИРУЕТ эти идентификаторы GUID в объект [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="03e18-126">The **GetSupportedEvents** method retrieves the GUIDs for each event supported by the service and copies those GUIDs into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="03e18-127">Следующий код иллюстрирует получение поддерживаемых событий службы.</span><span class="sxs-lookup"><span data-stu-id="03e18-127">The following code illustrates retrieving supported service events.</span></span>


```C++
// List all supported events on the service
void ListSupportedEvents(
    IPortableDeviceService* pService)
{
    HRESULT hr          = S_OK;
    DWORD   dwNumEvents = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pEvents;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all events supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedEvents(&pEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get supported events from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported events found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pEvents->GetCount(&dwNumEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Events Found on the service\n\n", dwNumEvents);

    // Loop through each event and display it
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
                    DisplayEvent(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="03e18-128">После того как метод **листсуппортедевентс** извлекает идентификаторы GUID, представляющие каждое событие, поддерживаемое данной службой, оно вызывает метод **дисплайевент** для получения данных, относящихся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="03e18-128">After the **ListSupportedEvents** method retrieves the GUIDs representing each event supported by the given service, it invokes the **DisplayEvent** method to retrieve event-specific data.</span></span> <span data-ttu-id="03e18-129">Эти данные включают имя события, его параметры (вещание или автозапуск), GUID параметров, типы параметров и т. д.</span><span class="sxs-lookup"><span data-stu-id="03e18-129">This data includes the event name, its options (broadcast or autoplay), parameter GUIDs, parameter types, and so on.</span></span>

<span data-ttu-id="03e18-130">Метод **дисплайевент** вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетевентаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) для получения коллекции атрибутов для данного события.</span><span class="sxs-lookup"><span data-stu-id="03e18-130">The **DisplayEvent** method invokes the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method to retrieve a collection of attributes for the given event.</span></span> <span data-ttu-id="03e18-131">Затем он вызывает метод [**ипортабледевицевалуес:: GetStringValue**](iportabledevicevalues-getstringvalue.md) и запрашивает, что драйвер возвращает понятное имя для данного события.</span><span class="sxs-lookup"><span data-stu-id="03e18-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a user-friendly name for the given event.</span></span> <span data-ttu-id="03e18-132">Затем **дисплайевент** вызывает метод [**Ипортабледевицевалуес:: жетипортабледевицевалуесвалуе**](iportabledevicevalues-getiportabledevicevaluesvalue.md) для получения параметров события.</span><span class="sxs-lookup"><span data-stu-id="03e18-132">Next, **DisplayEvent** calls the [**IPortableDeviceValues::GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) to retrieve the event options.</span></span> <span data-ttu-id="03e18-133">Наконец, Дисплайевент вызывает метод [**ипортабледевицевалуес:: жетипортабледевицекэйколлектионвалуе**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) для получения списка параметров события.</span><span class="sxs-lookup"><span data-stu-id="03e18-133">Finally, DisplayEvent calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the list of event parameters.</span></span> <span data-ttu-id="03e18-134">Он передает данные, возвращаемые этими методами, в вспомогательные функции **дисплайевентоптионс** и **дисплайевентпараметерс** , которые отображают параметры и сведения о параметрах для данного события.</span><span class="sxs-lookup"><span data-stu-id="03e18-134">It passes the data returned by these methods to the **DisplayEventOptions** and the **DisplayEventParameters** helper functions, which render the options and parameter information for the given event.</span></span>

<span data-ttu-id="03e18-135">В следующем коде используется метод **дисплайевент** .</span><span class="sxs-lookup"><span data-stu-id="03e18-135">The following code uses the **DisplayEvent** method.</span></span>


```C++
// Display basic information about an event
void DisplayEvent(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Event)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the event attributes which describe the event
    HRESULT hr = pCapabilities->GetEventAttributes(Event, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the event attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the event if it is available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_EVENT_ATTRIBUTE_NAME, &pszFormatName);
        if (SUCCEEDED(hr))
        {
            printf("%ws\n", pszFormatName);
        }
        else
        {
            printf("%ws\n", (PWSTR)CGuidToString(Event));
        }       

        // Display the event options
        hr = pAttributes->GetIPortableDeviceValuesValue(WPD_EVENT_ATTRIBUTE_OPTIONS, &pOptions);
        if (SUCCEEDED(hr))
        {
            DisplayEventOptions(pOptions);
        }
        else
        {
            printf("! Failed to get the event options, hr = 0x%lx\n", hr);
        }       

        // Display the event parameters
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_EVENT_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayEventParameters(pCapabilities, Event, pParameters);
        }
        else
        {
            printf("! Failed to get the event parameters, hr = 0x%lx\n", hr);
        }       
        
        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



<span data-ttu-id="03e18-136">Вспомогательная функция **дисплайевентоптионс** получает объект [**ипортабледевицевалуес**](iportabledevicevalues.md) , содержащий данные параметра события.</span><span class="sxs-lookup"><span data-stu-id="03e18-136">The **DisplayEventOptions** helper function receives an [**IPortableDeviceValues**](iportabledevicevalues.md) object which contains the event's option data.</span></span> <span data-ttu-id="03e18-137">Затем он вызывает метод [**ипортабледевицевалуес:: жетбулвалуе**](iportabledevicevalues-getboolvalue.md) для получения данных параметров.</span><span class="sxs-lookup"><span data-stu-id="03e18-137">It then calls the [**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) method to retrieve the options data.</span></span> <span data-ttu-id="03e18-138">С помощью этих данных отображается строка, указывающая, поддерживаются ли параметры вещания и автозапуска.</span><span class="sxs-lookup"><span data-stu-id="03e18-138">Using this data, it renders a string indicating whether the broadcast and autoplay options are supported.</span></span>


```C++
// Display the basic event options.
void DisplayEventOptions(
    IPortableDeviceValues* pOptions)
{
    printf("\tEvent Options:\n");
    // Read the WPD_EVENT_OPTION_IS_BROADCAST_EVENT value to see if the event is
    // a broadcast event. If the read fails, assume FALSE
    BOOL  bIsBroadcastEvent = FALSE;
    pOptions->GetBoolValue(WPD_EVENT_OPTION_IS_BROADCAST_EVENT, &bIsBroadcastEvent);
    printf("\tWPD_EVENT_OPTION_IS_BROADCAST_EVENT = %ws\n",bIsBroadcastEvent ? L"TRUE" : L"FALSE");
}
```



## <a name="related-topics"></a><span data-ttu-id="03e18-139">См. также</span><span class="sxs-lookup"><span data-stu-id="03e18-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03e18-140">**ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="03e18-140">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="03e18-141">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="03e18-141">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="03e18-142">**ипортабледевицесервицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="03e18-142">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="03e18-143">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="03e18-143">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="03e18-144">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="03e18-144">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



