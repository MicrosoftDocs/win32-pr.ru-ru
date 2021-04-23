---
description: Получение возможностей отрисовки, поддерживаемых устройством
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: Получение возможностей отрисовки, поддерживаемых устройством
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523f1f9bbcaefe1c502c7c74252582fddcadad4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349342"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a><span data-ttu-id="17b59-103">Получение возможностей отрисовки, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="17b59-103">Retrieving the Rendering Capabilities Supported by a Device</span></span>

<span data-ttu-id="17b59-104">Портативные устройства Windows, которые поддерживают функциональную категорию отрисовки информации ( \_ \_ сведения о визуализации функциональной категории WPD \_ \_ ), возвращают сведения о отрисовке при запросе.</span><span class="sxs-lookup"><span data-stu-id="17b59-104">Windows Portable Devices that support the rendering information functional category (WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION) will return rendering information when queried.</span></span> <span data-ttu-id="17b59-105">Сведения о подготовке к просмотру описывают требования и ограничения, наложенные на приложения, пытающиеся записать содержимое на устройство.</span><span class="sxs-lookup"><span data-stu-id="17b59-105">The rendering information describes requirements and restrictions imposed on applications that attempt to write content to a device.</span></span>

<span data-ttu-id="17b59-106">Функция Листрендерингкапабилитинформатион, вспомогательная функция Суппортсфунктионалкатегори и вспомогательная функция Реадпрофилеинформатионпропертиес в модуле DeviceCapabilities. cpp демонстрируют получение возможностей отрисовки для выбранного устройства.</span><span class="sxs-lookup"><span data-stu-id="17b59-106">The ListRenderingCapabilityInformation function, the SupportsFunctionalCategory helper function, and the ReadProfileInformationProperties helper function in the DeviceCapabilities.cpp module demonstrate the retrieval of rendering capabilities for a selected device.</span></span>

<span data-ttu-id="17b59-107">Приложение может получать возможности отрисовки, поддерживаемые устройством, с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="17b59-107">Your application can retrieve the rendering capabilities supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="17b59-108">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="17b59-108">Interface</span></span>                                                                                      | <span data-ttu-id="17b59-109">Описание</span><span class="sxs-lookup"><span data-stu-id="17b59-109">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="17b59-110">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="17b59-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="17b59-111">Предоставляет доступ к интерфейсу Ипортабледевицепропертиес.</span><span class="sxs-lookup"><span data-stu-id="17b59-111">Provides access to the IPortableDeviceProperties interface.</span></span> |
| [<span data-ttu-id="17b59-112">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="17b59-112">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="17b59-113">Предоставляет доступ к методам, относящимся к конкретному свойству.</span><span class="sxs-lookup"><span data-stu-id="17b59-113">Provides access to the property-specific methods.</span></span>           |
| [<span data-ttu-id="17b59-114">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="17b59-114">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="17b59-115">Используется для хранения ключей свойств для данного профиля.</span><span class="sxs-lookup"><span data-stu-id="17b59-115">Used to store the property keys for the given profile.</span></span>      |
| [<span data-ttu-id="17b59-116">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="17b59-116">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="17b59-117">Используется для хранения значений свойств заданного профиля.</span><span class="sxs-lookup"><span data-stu-id="17b59-117">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="17b59-118">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="17b59-118">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="17b59-119">Используется для хранения значений свойств заданного профиля.</span><span class="sxs-lookup"><span data-stu-id="17b59-119">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="17b59-120">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="17b59-120">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="17b59-121">Используется для хранения значений свойств заданного профиля.</span><span class="sxs-lookup"><span data-stu-id="17b59-121">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="17b59-122">**Интерфейс Ипортабледевицевалуесколлектион**</span><span class="sxs-lookup"><span data-stu-id="17b59-122">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="17b59-123">Используется для хранения значений свойств заданного профиля.</span><span class="sxs-lookup"><span data-stu-id="17b59-123">Used store the property values for the given profile.</span></span>       |



 

<span data-ttu-id="17b59-124">Одна из первых задач, выполняемых примером приложения, — определить, поддерживает ли выбранное устройство вывод списка возможностей отрисовки.</span><span class="sxs-lookup"><span data-stu-id="17b59-124">One of the first tasks accomplished by the sample application is to determine whether the selected device is capable of listing rendering capabilities.</span></span> <span data-ttu-id="17b59-125">Вспомогательная функция Суппортсфунктионалкатегори определяет, является ли это случай, вызывая вспомогательную функцию Листрендерингкапабилитинформатион и передавая \_ \_ сведения о визуализации функциональной категории WPD в \_ \_ качестве второго аргумента.</span><span class="sxs-lookup"><span data-stu-id="17b59-125">The SupportsFunctionalCategory helper function determines whether this is the case by calling the ListRenderingCapabilityInformation helper function and passing WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION as the second argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SupportsFunctionalCategory(pDevice, WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION) == FALSE)
{
    printf("This device does not support device rendering information to display\n");
    return;
}
```



<span data-ttu-id="17b59-126">Если устройство поддерживает перечисление возможностей отрисовки, следующий шаг влечет за собой извлечение объекта [**ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) и вызов метода [**жетфунктионалобжектс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) для получения идентификатора объекта для объекта сведений о подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="17b59-126">If the device is capable of listing rendering capabilities, the next step entails retrieving an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object and invoking the [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method to retrieve an object identifier for the rendering-information object.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get the functional object identifier for the rendering information object
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalObjects(WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION, &pRenderingInfoObjects);
    if (FAILED(hr))
    {
        printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="17b59-127">Следующим шагом является сохранение идентификатора объекта подготовки отчетов, который был только что получен в строковой переменной (Стррендерингинфубжектид), а затем вызов вспомогательной функции Реадпрофилеинформатионпропертиес.</span><span class="sxs-lookup"><span data-stu-id="17b59-127">The next step is to store the rendering-information object identifier that was just retrieved in a string variable (strRenderingInfoObjectID), and then to call the ReadProfileInformationProperties helper function.</span></span> <span data-ttu-id="17b59-128">(Переменная, Стррендерингинфубжектид, передается в качестве второго аргумента вспомогательной функции.)</span><span class="sxs-lookup"><span data-stu-id="17b59-128">(The variable, strRenderingInfoObjectID, is passed as the second argument to the helper function.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SUCCEEDED(hr))
{
    PROPVARIANT pv = {0};
    PropVariantInit(&pv);
    hr = pRenderingInfoObjects->GetAt(0, &pv);
    if ((SUCCEEDED(hr))    &&
        (pv.vt== VT_LPWSTR) )
    {
        strRenderingInfoObjectID = pv.pwszVal;
    }
    else
    {
        printf("! Failed to get first rendering object's identifier, hr = 0x%lx\n", hr);
    }

    PropVariantClear(&pv);
}

if (SUCCEEDED(hr))
{
    hr = ReadProfileInformationProperties(pDevice,
                                          strRenderingInfoObjectID,
                                          &pRenderingInfoProfiles);
    // Error output statements are performed by the helper function, so they
    // are omitted here.
}
```



<span data-ttu-id="17b59-129">Одной из первых задач, выполняемых вспомогательной функцией, является получение объекта [**ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , который будет использоваться для доступа к методам, связанным с содержимым.</span><span class="sxs-lookup"><span data-stu-id="17b59-129">One of the first tasks accomplished by the helper function is to retrieve an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to access the content-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="17b59-130">Затем вспомогательная функция получает объект [**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) , который будет использоваться для доступа к методам, относящимся к свойству.</span><span class="sxs-lookup"><span data-stu-id="17b59-130">Next, the helper function retrieves an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) object, which it will use to access the property-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="17b59-131">Следующим шагом является создание объекта [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , в котором хранятся ключи свойств для данных отрисовки.</span><span class="sxs-lookup"><span data-stu-id="17b59-131">The next step is to create an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object into which the property keys for the rendering information are stored.</span></span> <span data-ttu-id="17b59-132">После создания объекта вызывается метод [**ипортабледевицекэйколлектион:: Add**](iportabledevicekeycollection-add.md) , чтобы добавить необходимые ключи.</span><span class="sxs-lookup"><span data-stu-id="17b59-132">Once the object is created, the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method is invoked to add the necessary keys.</span></span> <span data-ttu-id="17b59-133">(Необходимо добавить эти ключи, чтобы в последующих шагах можно было получить соответствующие профили подготовки к просмотру.)</span><span class="sxs-lookup"><span data-stu-id="17b59-133">(It is necessary to add these keys so that the corresponding rendering profiles can be retrieved in the subsequent steps.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IPortableDeviceKeyCollection,
                      (VOID**) &pPropertiesToRead);
if (SUCCEEDED(hr))
{
    // Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_RENDERING_INFORMATION_PROFILES);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_RENDERING_INFORMATION_PROFILES to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="17b59-134">Следующим шагом является получение значений свойств из драйвера устройства путем вызова метода [**ипортабледевицепропертиес::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) GetNext.</span><span class="sxs-lookup"><span data-stu-id="17b59-134">The next step is to retrieve the property values from the device driver by calling the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(wszFunctionalObjectID, // The object whose properties we are reading
                                pPropertiesToRead,     // The properties we want to read
                                &pObjectProperties);   // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", wszFunctionalObjectID, hr);
    }
}
```



<span data-ttu-id="17b59-135">Следующий шаг извлекает профиль сведений о подготовке к просмотру и сохраняет его в аргументе Ппрендерингинфопрофилес.</span><span class="sxs-lookup"><span data-stu-id="17b59-135">The next step retrieves the rendering-information profile and stores it in the ppRenderingInfoProfiles argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pObjectProperties->GetIPortableDeviceValuesCollectionValue(WPD_RENDERING_INFORMATION_PROFILES,
                                                                    &pRenderingInfoProfiles);
    if (FAILED(hr))
    {
        printf("! Failed to get WPD_RENDERING_INFORMATION_PROFILES from rendering information, hr= 0x%lx\n",  hr);
    }
}

// QueryInterface the interface into the out-going parameters.
if (SUCCEEDED(hr))
{
    hr = pRenderingInfoProfiles->QueryInterface(IID_PPV_ARGS(ppRenderingInfoProfiles));
    if (FAILED(hr))
    {
        printf("! Failed to QueryInterface for IPortableDeviceValuesCollection (Rendering information profiles), hr= 0x%lx\n",  hr);
    }
}
```



<span data-ttu-id="17b59-136">После того как вспомогательная функция считывает \_ \_ свойства профиля данных визуализации WPD \_ , отображаются профили подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="17b59-136">After the helper function reads the WPD\_RENDERING\_INFORMATION\_PROFILES properties, the rendering profiles are displayed.</span></span> <span data-ttu-id="17b59-137">Эти профили отображаются вспомогательной функцией Дисплайрендерингпрофиле.</span><span class="sxs-lookup"><span data-stu-id="17b59-137">These profiles are displayed by the DisplayRenderingProfile helper function.</span></span>


```C++
void DisplayRenderingProfile(
    IPortableDeviceValues* pProfile)
{
    HRESULT hr = S_OK;
    if (pProfile == NULL)
    {
        return;
    }

    if (SUCCEEDED(hr))
    {
        DWORD dwTotalBitrate    = 0;
        DWORD dwChannelCount    = 0;
        DWORD dwAudioFormatCode = 0;
        GUID  guidFormat        = WPD_OBJECT_FORMAT_UNSPECIFIED;

        // Display WPD_MEDIA_TOTAL_BITRATE
        hr = pProfile->GetUnsignedIntegerValue(WPD_MEDIA_TOTAL_BITRATE, &dwTotalBitrate);
        if (SUCCEEDED(hr))
        {
            printf("Total Bitrate: %d\n", dwTotalBitrate);
        }

        // If we fail to read the total bitrate as a single value, then it must be
        // a valid value set.  (i.e. returning IPortableDeviceValues as the value which
        // contains properties describing the valid values for this property.)
        if (hr == DISP_E_TYPEMISMATCH)
        {
            CComPtr<IPortableDeviceValues> pExpectedValues;
            hr = pProfile->GetIPortableDeviceValuesValue(WPD_MEDIA_TOTAL_BITRATE, &pExpectedValues);
            if (SUCCEEDED(hr))
            {
                printf("Total Bitrate: ");
                DisplayExpectedValues(pExpectedValues);
            }
        }

        // If we are still a failure here, report the error
        if (FAILED(hr))
        {

            printf("! Failed to get WPD_MEDIA_TOTAL_BITRATE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_CHANNEL_COUNT
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_CHANNEL_COUNT, &dwChannelCount);
        if (SUCCEEDED(hr))
        {
            printf("Channel Count: %d\n", dwChannelCount);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_CHANNEL_COUNT from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_FORMAT_CODE
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_FORMAT_CODE,   &dwAudioFormatCode);
        if (SUCCEEDED(hr))
        {
            printf("Audio Format Code: %d\n", dwAudioFormatCode);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_FORMAT_CODE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_OBJECT_FORMAT
        hr = pProfile->GetGuidValue(WPD_OBJECT_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("Object Format: %ws\n", (LPWSTR)CComBSTR(guidFormat));
        }
        else
        {
            printf("! Failed to get WPD_OBJECT_FORMAT from rendering profile, hr = 0x%lx\n",hr);
        }
    }
}
```



<span data-ttu-id="17b59-138">Обратите внимание, что поскольку профили подготовки к просмотру статичны, приложение может считывать профили и сохранять их локально (вместо доступа к устройству каждый раз, когда требуются данные).</span><span class="sxs-lookup"><span data-stu-id="17b59-138">Note that since the rendering profiles are static, your application may choose to read the profiles and store them locally (instead of accessing the device each time the data is needed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="17b59-139">См. также</span><span class="sxs-lookup"><span data-stu-id="17b59-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17b59-140">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="17b59-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="17b59-141">**Интерфейс Ипортабледевицекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="17b59-141">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="17b59-142">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="17b59-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="17b59-143">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="17b59-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="17b59-144">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="17b59-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="17b59-145">**Интерфейс Ипортабледевицевалуесколлектион**</span><span class="sxs-lookup"><span data-stu-id="17b59-145">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> <dt>

[<span data-ttu-id="17b59-146">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="17b59-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



