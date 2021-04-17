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
# <a name="retrieving-supported-service-events"></a>Получение поддерживаемых событий службы

Приложение Впдсервицесаписампле содержит код, демонстрирующий, как приложение может извлекать события, поддерживаемые данной службой контактов, вызывая методы для следующих интерфейсов.



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Интерфейс                                                                            | Описание                                                                                           |
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Используется для получения интерфейса **ипортабледевицесервицекапабилитиес** для доступа к поддерживаемым событиям. |
| [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Предоставляет доступ к поддерживаемым событиям и атрибутам событий.                                         |
| [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Содержит список поддерживаемых событий.                                                                |
| [**ипортабледевицевалуес**](iportabledevicevalues.md)                               | Содержит атрибуты для данного события.                                                            |



 

Когда пользователь выбирает параметр "4" в командной строке, приложение вызывает метод **листсуппортедевентс** , который находится в модуле сервицекапабилитиес. cpp.

Обратите внимание, что перед получением списка событий пример приложения открывает службу контактов на подключенном устройстве.

В WPD событие описывается по имени, параметрам и параметрам. Имя события является строкой, понятной для сценария, например "Микустомевент". Параметры события указывают, будет ли заданное событие пересылаться всем клиентам и поддерживает ли это событие автозапуск. Атрибуты параметра события включают PROPERTYKEY и VARTYPE данного параметра.

Четыре метода в модуле Сервицекапабилитиес. cpp поддерживают получение поддерживаемых событий для данной службы Contacts: **листсуппортедевентс**, **дисплайевент**, **дисплайевентоптионс** и **дисплайевентпараметерс**. Метод **листсуппортедевентс** извлекает количество поддерживаемых событий и идентификатор GUID для каждого события. Метод **дисплайевент** отображает имя события или идентификатор GUID, а затем вызывает **дисплайевентоптионс** и **дисплайевентпараметерс** для отображения данных, связанных с событиями.

Метод **листсуппортедевентс** вызывает метод [**Ипортабледевицесервице:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Используя этот интерфейс, он получает поддерживаемые события, вызывая метод [**ипортабледевицесервицекапабилитиес:: жетсуппортедевентс**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) . Метод **жетсуппортедевентс** извлекает идентификаторы GUID для каждого события, поддерживаемого службой, и КОПИРУЕТ эти идентификаторы GUID в объект [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) .

Следующий код иллюстрирует получение поддерживаемых событий службы.


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



После того как метод **листсуппортедевентс** извлекает идентификаторы GUID, представляющие каждое событие, поддерживаемое данной службой, оно вызывает метод **дисплайевент** для получения данных, относящихся к конкретному событию. Эти данные включают имя события, его параметры (вещание или автозапуск), GUID параметров, типы параметров и т. д.

Метод **дисплайевент** вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетевентаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) для получения коллекции атрибутов для данного события. Затем он вызывает метод [**ипортабледевицевалуес:: GetStringValue**](iportabledevicevalues-getstringvalue.md) и запрашивает, что драйвер возвращает понятное имя для данного события. Затем **дисплайевент** вызывает метод [**Ипортабледевицевалуес:: жетипортабледевицевалуесвалуе**](iportabledevicevalues-getiportabledevicevaluesvalue.md) для получения параметров события. Наконец, Дисплайевент вызывает метод [**ипортабледевицевалуес:: жетипортабледевицекэйколлектионвалуе**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) для получения списка параметров события. Он передает данные, возвращаемые этими методами, в вспомогательные функции **дисплайевентоптионс** и **дисплайевентпараметерс** , которые отображают параметры и сведения о параметрах для данного события.

В следующем коде используется метод **дисплайевент** .


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



Вспомогательная функция **дисплайевентоптионс** получает объект [**ипортабледевицевалуес**](iportabledevicevalues.md) , содержащий данные параметра события. Затем он вызывает метод [**ипортабледевицевалуес:: жетбулвалуе**](iportabledevicevalues-getboolvalue.md) для получения данных параметров. С помощью этих данных отображается строка, указывающая, поддерживаются ли параметры вещания и автозапуска.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)
</dt> <dt>

[**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[впдсервицесаписампле](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



