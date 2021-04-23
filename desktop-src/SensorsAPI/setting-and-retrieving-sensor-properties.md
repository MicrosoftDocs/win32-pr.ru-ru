---
description: В этом разделе описывается извлечение и задание значений для свойств датчика. Интерфейс Исенсор предоставляет методы для установки и получения значений для свойств датчика.
ms.assetid: 7d10e5b4-bae7-4564-84eb-75c6a2eeef8f
title: Извлечение и задание свойств датчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f64bf0e253f47ae2d8cd1f4945f3b87aa3406b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663796"
---
# <a name="retrieving-and-setting-sensor-properties"></a><span data-ttu-id="05821-104">Извлечение и задание свойств датчика</span><span class="sxs-lookup"><span data-stu-id="05821-104">Retrieving and Setting Sensor Properties</span></span>

<span data-ttu-id="05821-105">В этом разделе описывается извлечение и задание значений для свойств датчика.</span><span class="sxs-lookup"><span data-stu-id="05821-105">This topic describes how to retrieve and set values for sensor properties.</span></span> <span data-ttu-id="05821-106">Интерфейс [**исенсор**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) предоставляет методы для установки и получения значений для свойств датчика.</span><span class="sxs-lookup"><span data-stu-id="05821-106">The [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface provides the methods to set and retrieve values for sensor properties.</span></span>

## <a name="retrieving-sensor-properties"></a><span data-ttu-id="05821-107">Получение свойств датчика</span><span class="sxs-lookup"><span data-stu-id="05821-107">Retrieving Sensor Properties</span></span>

<span data-ttu-id="05821-108">Вы можете извлечь некоторые значения свойств с датчика, прежде чем пользователь его включил.</span><span class="sxs-lookup"><span data-stu-id="05821-108">You can retrieve some property values from a sensor before the user has enabled it.</span></span> <span data-ttu-id="05821-109">Такие сведения, как имя изготовителя или модель датчика, могут помочь решить, может ли программа использовать датчик.</span><span class="sxs-lookup"><span data-stu-id="05821-109">Information such as the manufacturer's name or the model of the sensor can help you to decide whether your program can use the sensor.</span></span>

<span data-ttu-id="05821-110">Можно выбрать получение одного значения свойства или получение коллекции значений свойств вместе.</span><span class="sxs-lookup"><span data-stu-id="05821-110">You can choose to retrieve a single property value, or to retrieve a collection of property values together.</span></span> <span data-ttu-id="05821-111">Чтобы получить единственное значение, вызовите [**исенсор:: Property**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span><span class="sxs-lookup"><span data-stu-id="05821-111">To retrieve single value, call [**ISensor::GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span></span> <span data-ttu-id="05821-112">Чтобы получить коллекцию значений, вызовите метод [**исенсор::-Properties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span><span class="sxs-lookup"><span data-stu-id="05821-112">To retrieve a collection of values, call [**ISensor::GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span></span> <span data-ttu-id="05821-113">Вы можете получить все свойства датчика, передав **значение NULL** через первый параметр в **исенсор::-Properties**.</span><span class="sxs-lookup"><span data-stu-id="05821-113">You can retrieve all properties for a sensor by passing **NULL** through the first parameter to **ISensor::GetProperties**.</span></span>

<span data-ttu-id="05821-114">В следующем примере кода создается вспомогательная функция, которая выводит значение одного свойства.</span><span class="sxs-lookup"><span data-stu-id="05821-114">The following example code creates a helper function that prints the value of a single property.</span></span> <span data-ttu-id="05821-115">Функция получает указатель на датчик, из которого извлекается значение, и ключ свойства, который содержит свойство для печати.</span><span class="sxs-lookup"><span data-stu-id="05821-115">The function receives a pointer to the sensor from which to retrieve the value and a property key that contains the property to print.</span></span> <span data-ttu-id="05821-116">Функция может печатать значения для чисел, строк и **идентификаторов GUID** s, но не для других, более сложных типов.</span><span class="sxs-lookup"><span data-stu-id="05821-116">The function can print values for numbers, strings, and **GUID** s, but not other, more complex types.</span></span>


```C++
HRESULT PrintSensorProperty(ISensor* pSensor, REFPROPERTYKEY pk)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    PROPVARIANT pv = {};

    hr = pSensor->GetProperty(pk, &pv);

    if(SUCCEEDED(hr))
    {
        if(pv.vt == VT_UI4)  // Number
        {
            wprintf_s(L"\nSensor integer value: %u\n", pv.ulVal);
        }
        else if(pv.vt == VT_LPWSTR)  // String
        {
            wprintf_s(L"\nSensor string value: %s\n", pv.pwszVal);
        }
        else if(pv.vt == VT_CLSID)  // GUID
        {
            int iRet = 0;

            // Convert the GUID to a string.
            OLECHAR wszGuid[39] = {}; // Buffer for string.
            iRet = ::StringFromGUID2(*(pv.puuid), wszGuid, 39);

            assert(39 == iRet); // Count of characters returned for GUID.

            wprintf_s(L"\nSensor GUID value: %s\n", wszGuid);
        }
        else  // Interface or vector
        {
            wprintf_s(L"\nSensor property is a compound type. Unable to print value.");
        }
    }

    PropVariantClear(&pv);

    return hr;    
}
```



<span data-ttu-id="05821-117">В следующем примере кода создается функция, которая извлекает и печатает коллекцию свойств.</span><span class="sxs-lookup"><span data-stu-id="05821-117">The following example code creates a function that retrieves and prints a collection of properties.</span></span> <span data-ttu-id="05821-118">Набор свойств для печати определяется массивом с именем Сенсорпропертиес.</span><span class="sxs-lookup"><span data-stu-id="05821-118">The set of properties to print is defined by the array named SensorProperties.</span></span>


```C++
HRESULT PrintSensorProperties(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    DWORD cVals = 0; // Count of returned properties.
    IPortableDeviceKeyCollection* pKeys = NULL; // Input
    IPortableDeviceValues* pValues = NULL;  // Output

    // Properties to print.
    const PROPERTYKEY SensorProperties[] =
    {
        SENSOR_PROPERTY_MANUFACTURER,
        SENSOR_PROPERTY_SERIAL_NUMBER,
        SENSOR_PROPERTY_DESCRIPTION,
        SENSOR_PROPERTY_FRIENDLY_NAME
    };

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER,                                 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        // Add the properties to the key collection.
        for (DWORD dwIndex = 0; dwIndex < ARRAYSIZE(SensorProperties); dwIndex++)
        {
            hr = pKeys->Add(SensorProperties[dwIndex]);

            if(FAILED(hr))
            {
                // Unexpected.
                // This example returns the failed HRESULT.
                // You may choose to ignore failures, here.
                break;
            }
        }
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the properties from the sensor.
        hr = pSensor->GetProperties(pKeys, &pValues);
    }

    if(SUCCEEDED(hr))
    {
        // Get the number of values returned.        
        hr = pValues->GetCount(&cVals);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk; // Keys
        PROPVARIANT pv = {}; // Values

        // Loop through the values;
        for (DWORD i = 0; i < cVals; i++)
        {
            // Get the value at the current index.
            hr = pValues->GetAt(i, &pk, &pv);

            if(SUCCEEDED(hr))
            { 
                // Find and print the property.
                if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_MANUFACTURER))
                {
                    wprintf_s(L"\nManufacturer: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_SERIAL_NUMBER))
                {
                    wprintf_s(L"Serial number: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_FRIENDLY_NAME))
                {
                    wprintf_s(L"Friendly name: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_DESCRIPTION))
                {
                    wprintf_s(L"Description: %s\n", pv.pwszVal);
                }
            }

            PropVariantClear(&pv);
        } // end i loop        
    }

    SafeRelease(&pKeys);
    SafeRelease(&pValues);

    return hr;
};
```



## <a name="setting-sensor-properties"></a><span data-ttu-id="05821-119">Настройка свойств датчика</span><span class="sxs-lookup"><span data-stu-id="05821-119">Setting Sensor Properties</span></span>

<span data-ttu-id="05821-120">Прежде чем можно будет задать значения свойств для датчика, пользователь должен включить датчик.</span><span class="sxs-lookup"><span data-stu-id="05821-120">Before you can set property values for a sensor, the user must enable the sensor.</span></span> <span data-ttu-id="05821-121">Кроме того, не все свойства датчика могут быть установлены.</span><span class="sxs-lookup"><span data-stu-id="05821-121">Also, not all sensor properties can be set.</span></span>

<span data-ttu-id="05821-122">Чтобы задать одно или несколько значений свойств, вызовите метод [**исенсор:: SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span><span class="sxs-lookup"><span data-stu-id="05821-122">To set one or more values for properties, call [**ISensor::SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span></span> <span data-ttu-id="05821-123">Этот метод предоставляется с помощью указателя [ипортабледевицевалуес](/previous-versions//ms740012(v=vs.85)) , содержащего коллекцию свойств, которые необходимо задать, и связанные с ними значения.</span><span class="sxs-lookup"><span data-stu-id="05821-123">You provide this method with an [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) pointer that contains the collection of properties to set, and their associated values.</span></span> <span data-ttu-id="05821-124">Метод возвращает соответствующий интерфейс [ипортабледевицевалуес](/previous-versions//ms740012(v=vs.85)) , который может содержать коды ошибок для свойств, которые не могут быть заданы.</span><span class="sxs-lookup"><span data-stu-id="05821-124">The method returns a corresponding [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface that may contain error codes for properties that could not be set.</span></span>

<span data-ttu-id="05821-125">В следующем примере кода создается вспомогательная функция, которая задает новое значение \_ \_ \_ свойства интервала текущего отчета для свойства датчика \_ .</span><span class="sxs-lookup"><span data-stu-id="05821-125">The following example code creates a helper function that sets a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="05821-126">Функция принимает указатель на датчик, для которого задается свойство, и значение **ulong** , указывающее, какой интервал времени должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="05821-126">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span> <span data-ttu-id="05821-127">(Обратите внимание, что установка значения для этого конкретного свойства не гарантирует, что датчик примет указанное значение.</span><span class="sxs-lookup"><span data-stu-id="05821-127">(Note that setting a value for this particular property does not guarantee that the sensor will accept the specified value.</span></span> <span data-ttu-id="05821-128">Сведения о том, как работает это свойство, см. в разделе [**Свойства датчика**](sensor-properties.md) .)</span><span class="sxs-lookup"><span data-stu-id="05821-128">See [**Sensor Properties**](sensor-properties.md) for information about how this property works.)</span></span>


```C++
HRESULT SetCurrentReportInterval(ISensor* pSensor, ULONG ulNewInterval)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    IPortableDeviceValues* pPropsToSet = NULL; // Input
    IPortableDeviceValues* pPropsReturn = NULL; // Output

    // Create the input object.
    hr = CoCreateInstance(__uuidof(PortableDeviceValues),
                            NULL,
                            CLSCTX_INPROC_SERVER,                           
                            IID_PPV_ARGS(&pPropsToSet));

    if(SUCCEEDED(hr))
    {
        // Add the current report interval property.
        hr = pPropsToSet->SetUnsignedIntegerValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, ulNewInterval);
    }

    if(SUCCEEDED(hr))
    {
        // Only setting a single property, here.
        hr = pSensor->SetProperties(pPropsToSet, &pPropsReturn);
    }

    // Test for failure.
    if(hr == S_FALSE)
    {
        HRESULT hrError = S_OK;
      
        // Check results for failure.
        hr = pPropsReturn->GetErrorValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, &hrError);

        if(SUCCEEDED(hr))
        {
            // Print an error message.
            wprintf_s(L"\nSetting current report interval failed with error 0x%X\n", hrError);

            // Return the error code.
            hr = hrError;
        }
    }
    else if(hr == E_ACCESSDENIED)
    {
        // No permission. Take appropriate action.
    }

    SafeRelease(&pPropsToSet);
    SafeRelease(&pPropsReturn);
   
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="05821-129">См. также</span><span class="sxs-lookup"><span data-stu-id="05821-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05821-130">**Свойства датчика**</span><span class="sxs-lookup"><span data-stu-id="05821-130">**Sensor Properties**</span></span>](sensor-properties.md)
</dt> </dl>

 

 
