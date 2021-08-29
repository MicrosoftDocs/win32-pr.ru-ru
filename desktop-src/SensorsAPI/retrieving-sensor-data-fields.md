---
description: В этом разделе описывается, как получить данные из датчика — синхронно и асинхронно.
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: Получение значений данных датчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e240b9bc14d917db0e0c4280ad957aa139369eb7762abfcd69441d25e66857d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960034"
---
# <a name="retrieving-sensor-data-values"></a>Получение значений данных датчика

В этом разделе описывается, как получить данные из датчика — синхронно и асинхронно.

## <a name="retrieving-data-synchronously"></a>Синхронное получение данных

Данные датчика можно получить синхронно путем вызова [**исенсор:: GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).

В следующем примере кода извлекается отчет с данными датчика, а затем извлекаются три отдельных значения полей данных. Пример датчика предоставляет пользовательские данные о текущем местном времени в полях данных в часах, минутах и секундах. Переменная с именем Псенсор содержит указатель на [**исенсор**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) , представляющий датчик, предоставляющий данные.


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



## <a name="retrieving-data-asynchronously"></a>Асинхронное получение данных

Данные датчика можно получить асинхронно путем регистрации, чтобы получить событие [**исенсоревентс:: ондатаупдатед**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) . Сведения о получении обратных вызовов событий датчика см. в разделе [Использование событий API датчика](using-sensor-api-events.md).

В следующем примере кода показана реализация [**исенсоревентс:: ондатаупдатед**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) , которая получает значения данных из отчета данных, предоставленного событием. Пример датчика предоставляет пользовательские данные о текущем местном времени в полях данных в часах, минутах и секундах.


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



 

 
