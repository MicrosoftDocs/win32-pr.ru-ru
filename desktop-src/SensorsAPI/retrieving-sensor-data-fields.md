---
description: В этом разделе описывается, как получить данные из датчика — синхронно и асинхронно.
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: Получение значений данных датчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4642f120e549cd77b1b37610037092facf2ead1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662274"
---
# <a name="retrieving-sensor-data-values"></a><span data-ttu-id="e4291-103">Получение значений данных датчика</span><span class="sxs-lookup"><span data-stu-id="e4291-103">Retrieving Sensor Data Values</span></span>

<span data-ttu-id="e4291-104">В этом разделе описывается, как получить данные из датчика — синхронно и асинхронно.</span><span class="sxs-lookup"><span data-stu-id="e4291-104">This topic describes how to retrieve data from a sensor, synchronously and asynchronously.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="e4291-105">Синхронное получение данных</span><span class="sxs-lookup"><span data-stu-id="e4291-105">Retrieving Data Synchronously</span></span>

<span data-ttu-id="e4291-106">Данные датчика можно получить синхронно путем вызова [**исенсор:: GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span><span class="sxs-lookup"><span data-stu-id="e4291-106">You can retrieve sensor data synchronously by calling [**ISensor::GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span></span>

<span data-ttu-id="e4291-107">В следующем примере кода извлекается отчет с данными датчика, а затем извлекаются три отдельных значения полей данных.</span><span class="sxs-lookup"><span data-stu-id="e4291-107">The following example code retrieves a sensor data report, and then retrieves three individual data field values.</span></span> <span data-ttu-id="e4291-108">Пример датчика предоставляет пользовательские данные о текущем местном времени в полях данных в часах, минутах и секундах.</span><span class="sxs-lookup"><span data-stu-id="e4291-108">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span> <span data-ttu-id="e4291-109">Переменная с именем Псенсор содержит указатель на [**исенсор**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) , представляющий датчик, предоставляющий данные.</span><span class="sxs-lookup"><span data-stu-id="e4291-109">The variable named pSensor contains a pointer to [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) that represents the sensor that supplies the data.</span></span>


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
  
if(SUCCEEDED(hr))
{
    PROPVARIANT var = {};

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);        

    if(SUCCEEDED(hr))
    {
        // Print the local time to the console window.
        wprintf_s(L"\nCurrent local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (synchronous)\n\n", ulHour, ulMinute, ulSecond);
    }

```



## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="e4291-110">Асинхронное получение данных</span><span class="sxs-lookup"><span data-stu-id="e4291-110">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="e4291-111">Данные датчика можно получить асинхронно путем регистрации, чтобы получить событие [**исенсоревентс:: ондатаупдатед**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) .</span><span class="sxs-lookup"><span data-stu-id="e4291-111">You can receive sensor data asynchronously by registering to receive the [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="e4291-112">Сведения о получении обратных вызовов событий датчика см. в разделе [Использование событий API датчика](using-sensor-api-events.md).</span><span class="sxs-lookup"><span data-stu-id="e4291-112">To understand how to receive sensor event callbacks, see [Using Sensor API Events](using-sensor-api-events.md).</span></span>

<span data-ttu-id="e4291-113">В следующем примере кода показана реализация [**исенсоревентс:: ондатаупдатед**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) , которая получает значения данных из отчета данных, предоставленного событием.</span><span class="sxs-lookup"><span data-stu-id="e4291-113">The following example code shows an implementation of [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) that retrieves data values from the data report provided by the event.</span></span> <span data-ttu-id="e4291-114">Пример датчика предоставляет пользовательские данные о текущем местном времени в полях данных в часах, минутах и секундах.</span><span class="sxs-lookup"><span data-stu-id="e4291-114">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span>


```C++
STDMETHODIMP OnDataUpdated(
        ISensor *pSensor,
        ISensorDataReport *pNewData)
{
    HRESULT hr = S_OK;

    if(NULL == pNewData ||
       NULL == pSensor)
    {
        return E_INVALIDARG;
    }

    ULONG ulHour = 0;
    ULONG ulMinute = 0;
    ULONG ulSecond = 0;

    PROPVARIANT var = {};

    hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        // Print
        wprintf_s(L"Current local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (asynchronous)\n", ulHour, ulMinute, ulSecond);
    }

    return hr;
}
```



 

 
