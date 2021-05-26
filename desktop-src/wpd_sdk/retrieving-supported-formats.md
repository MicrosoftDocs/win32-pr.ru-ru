---
description: Получение поддерживаемых форматов службы
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Получение поддерживаемых форматов службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73618f3450255ad470545ac472ad9f71238621e3
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423815"
---
# <a name="retrieving-supported-service-formats"></a>Получение поддерживаемых форматов службы

Приложение Впдсервицесаписампле содержит код, демонстрирующий, как приложение может извлекать форматы, поддерживаемые данной службой контактов, путем вызова методов интерфейсов, приведенных в следующей таблице.



| Интерфейс | Описание   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Используется для получения интерфейса **ипортабледевицесервицекапабилитиес** для доступа к поддерживаемым событиям. |
| [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Предоставляет доступ к поддерживаемым событиям и атрибутам событий.                                         |
| [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Содержит список поддерживаемых форматов.                                                               |
| [**ипортабледевицевалуес**](iportabledevicevalues.md)                               | Содержит атрибуты для заданного формата.                                                           |



 

Когда пользователь выбирает параметр "3" в командной строке, приложение вызывает метод **листсуппортедформатс** , который находится в модуле сервицекапабилитиес. cpp.

Обратите внимание, что перед получением списка событий пример приложения открывает службу контактов на подключенном устройстве.

В WPD формат описывается атрибутами, задающихи имя и (необязательно) тип MIME данного формата. Эти атрибуты определяются в файле заголовка Сепортабледевице. h. Описание поддерживаемых атрибутов см. в разделе [атрибуты](attributes.md) .

В случае с примером приложения, если Впдсервицесампледривер является единственным установленным устройством, драйвер возвращает два поддерживаемых формата для контактной службы: "Абстрактконтактформат" и "VCard2Format". Эти форматы соответствуют **\_ \_ \_ абстрактному \_ контактному формату объекта WPD** и **\_ \_ формату объекта WPD \_ VCARD2** атрибуты, обнаруженные в портабледевице. h.

Два метода в модуле Сервицекапабилитиес. cpp поддерживают получение поддерживаемых форматов для службы Contacts: **листсуппортедформатс** и **DisplayFormat**. Первый из них получает идентификатор GUID для каждого поддерживаемого формата. Последний преобразует этот идентификатор GUID в удобную для пользователя строку.

Метод **листсуппортедформатс** вызывает метод [**Ипортабледевицесервице:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Используя этот интерфейс, он получает Поддерживаемые форматы, вызывая метод [**ипортабледевицесервицекапабилитиес:: жетсуппортедформатс**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) . Метод **жетсуппортедформатс** извлекает идентификатор GUID для каждого формата, поддерживаемого службой, и копирует этот идентификатор GUID в объект [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) .

В следующем коде используется метод **листсуппортедформатс** .


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

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

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



После того как метод **листсуппортедформатс** извлекает идентификатор GUID для каждого формата, поддерживаемого данной службой, он вызывает метод **DisplayFormat** для вывода понятного имени скрипта для каждого формата. Например, "VCard2".

Метод **DisplayFormat** вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетформататтрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) для получения коллекции атрибутов для заданного GUID формата. Затем он вызывает метод [**ипортабледевицевалуес:: GetStringValue**](iportabledevicevalues-getstringvalue.md) и запрашивает, что драйвер возвращает понятное для сценария имя в заданном формате.

В следующем коде используется метод **DisplayFormat** .


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[впдсервицесаписампле](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



