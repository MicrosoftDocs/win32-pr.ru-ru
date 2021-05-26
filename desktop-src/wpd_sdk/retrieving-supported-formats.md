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
# <a name="retrieving-supported-service-formats"></a><span data-ttu-id="b6836-103">Получение поддерживаемых форматов службы</span><span class="sxs-lookup"><span data-stu-id="b6836-103">Retrieving Supported Service Formats</span></span>

<span data-ttu-id="b6836-104">Приложение Впдсервицесаписампле содержит код, демонстрирующий, как приложение может извлекать форматы, поддерживаемые данной службой контактов, путем вызова методов интерфейсов, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b6836-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the formats supported by a given Contacts service by calling methods of the interfaces in the following table.</span></span>



| <span data-ttu-id="b6836-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="b6836-105">Interface</span></span> | <span data-ttu-id="b6836-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b6836-106">Description</span></span>   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6836-107">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="b6836-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="b6836-108">Используется для получения интерфейса **ипортабледевицесервицекапабилитиес** для доступа к поддерживаемым событиям.</span><span class="sxs-lookup"><span data-stu-id="b6836-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="b6836-109">**ипортабледевицесервицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b6836-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="b6836-110">Предоставляет доступ к поддерживаемым событиям и атрибутам событий.</span><span class="sxs-lookup"><span data-stu-id="b6836-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="b6836-111">**ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="b6836-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="b6836-112">Содержит список поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="b6836-112">Contains the list of supported formats.</span></span>                                                               |
| [<span data-ttu-id="b6836-113">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="b6836-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="b6836-114">Содержит атрибуты для заданного формата.</span><span class="sxs-lookup"><span data-stu-id="b6836-114">Contains the attributes for a given format.</span></span>                                                           |



 

<span data-ttu-id="b6836-115">Когда пользователь выбирает параметр "3" в командной строке, приложение вызывает метод **листсуппортедформатс** , который находится в модуле сервицекапабилитиес. cpp.</span><span class="sxs-lookup"><span data-stu-id="b6836-115">When the user chooses option "3" at the command line, the application invokes the **ListSupportedFormats** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="b6836-116">Обратите внимание, что перед получением списка событий пример приложения открывает службу контактов на подключенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="b6836-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="b6836-117">В WPD формат описывается атрибутами, задающихи имя и (необязательно) тип MIME данного формата.</span><span class="sxs-lookup"><span data-stu-id="b6836-117">In WPD, a format is described by attributes that specify the name and (optionally) the MIME type of a given format.</span></span> <span data-ttu-id="b6836-118">Эти атрибуты определяются в файле заголовка Сепортабледевице. h.</span><span class="sxs-lookup"><span data-stu-id="b6836-118">These attributes are defined in thePortableDevice.h header file.</span></span> <span data-ttu-id="b6836-119">Описание поддерживаемых атрибутов см. в разделе [атрибуты](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="b6836-119">For a description of supported attributes, refer to the [Attributes](attributes.md) topic.</span></span>

<span data-ttu-id="b6836-120">В случае с примером приложения, если Впдсервицесампледривер является единственным установленным устройством, драйвер возвращает два поддерживаемых формата для контактной службы: "Абстрактконтактформат" и "VCard2Format".</span><span class="sxs-lookup"><span data-stu-id="b6836-120">In the case of the sample application, if the WpdServiceSampleDriver is the only installed device, the driver returns two supported formats for its Contact service: "AbstractContactFormat" and "VCard2Format".</span></span> <span data-ttu-id="b6836-121">Эти форматы соответствуют **\_ \_ \_ абстрактному \_ контактному формату объекта WPD** и **\_ \_ формату объекта WPD \_ VCARD2** атрибуты, обнаруженные в портабледевице. h.</span><span class="sxs-lookup"><span data-stu-id="b6836-121">These formats correspond to the **WPD\_OBJECT\_FORMAT\_ABSTRACT\_CONTACT** and the **WPD\_OBJECT\_FORMAT\_VCARD2** attributes found in PortableDevice.h.</span></span>

<span data-ttu-id="b6836-122">Два метода в модуле Сервицекапабилитиес. cpp поддерживают получение поддерживаемых форматов для службы Contacts: **листсуппортедформатс** и **DisplayFormat**.</span><span class="sxs-lookup"><span data-stu-id="b6836-122">Two methods in the ServiceCapabilities.cpp module support the retrieval of supported formats for the Contacts service: **ListSupportedFormats** and **DisplayFormat**.</span></span> <span data-ttu-id="b6836-123">Первый из них получает идентификатор GUID для каждого поддерживаемого формата.</span><span class="sxs-lookup"><span data-stu-id="b6836-123">The former retrieves the GUID identifier for each supported format.</span></span> <span data-ttu-id="b6836-124">Последний преобразует этот идентификатор GUID в удобную для пользователя строку.</span><span class="sxs-lookup"><span data-stu-id="b6836-124">The latter converts this GUID into a user-friendly string.</span></span>

<span data-ttu-id="b6836-125">Метод **листсуппортедформатс** вызывает метод [**Ипортабледевицесервице:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="b6836-125">The **ListSupportedFormats** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="b6836-126">Используя этот интерфейс, он получает Поддерживаемые форматы, вызывая метод [**ипортабледевицесервицекапабилитиес:: жетсуппортедформатс**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) .</span><span class="sxs-lookup"><span data-stu-id="b6836-126">Using this interface, it retrieves the supported formats by calling the [**IPortableDeviceServiceCapabilities::GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) method.</span></span> <span data-ttu-id="b6836-127">Метод **жетсуппортедформатс** извлекает идентификатор GUID для каждого формата, поддерживаемого службой, и копирует этот идентификатор GUID в объект [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b6836-127">The **GetSupportedFormats** method retrieves the GUID for each format supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="b6836-128">В следующем коде используется метод **листсуппортедформатс** .</span><span class="sxs-lookup"><span data-stu-id="b6836-128">The following code uses the **ListSupportedFormats** method.</span></span>


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



<span data-ttu-id="b6836-129">После того как метод **листсуппортедформатс** извлекает идентификатор GUID для каждого формата, поддерживаемого данной службой, он вызывает метод **DisplayFormat** для вывода понятного имени скрипта для каждого формата. Например, "VCard2".</span><span class="sxs-lookup"><span data-stu-id="b6836-129">After the **ListSupportedFormats** method retrieves the GUID for each format supported by the given service, it invokes the **DisplayFormat** method to display the script friendly name for each format; for example, "VCard2".</span></span>

<span data-ttu-id="b6836-130">Метод **DisplayFormat** вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетформататтрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) для получения коллекции атрибутов для заданного GUID формата.</span><span class="sxs-lookup"><span data-stu-id="b6836-130">The **DisplayFormat** method invokes the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method retrieve a collection of attributes for the given format GUID.</span></span> <span data-ttu-id="b6836-131">Затем он вызывает метод [**ипортабледевицевалуес:: GetStringValue**](iportabledevicevalues-getstringvalue.md) и запрашивает, что драйвер возвращает понятное для сценария имя в заданном формате.</span><span class="sxs-lookup"><span data-stu-id="b6836-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a script-friendly name for the given format.</span></span>

<span data-ttu-id="b6836-132">В следующем коде используется метод **DisplayFormat** .</span><span class="sxs-lookup"><span data-stu-id="b6836-132">The following code uses the **DisplayFormat** method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b6836-133">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b6836-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6836-134">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="b6836-134">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="b6836-135">**ипортабледевицесервицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b6836-135">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="b6836-136">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="b6836-136">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b6836-137">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="b6836-137">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



