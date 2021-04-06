---
description: Для получения объекта датчика используется интерфейс Исенсорманажер. Этот интерфейс можно считать корневым интерфейсом для API датчика. Чтобы использовать Исенсорманажер, необходимо сначала вызвать метод COM CoCreateInstance.
ms.assetid: 36631bae-f237-4951-9959-6ab6286bd1f7
title: Получение объекта датчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cda6ea04d1a0580c38aef5a0b9c4186b908300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991009"
---
# <a name="retrieving-a-sensor-object"></a>Получение объекта датчика

Для получения объекта датчика используется интерфейс [**исенсорманажер**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) . Этот интерфейс можно считать корневым интерфейсом для API датчика. Чтобы использовать **исенсорманажер**, необходимо сначала вызвать метод COM **CoCreateInstance** .

В следующем примере кода создается экземпляр диспетчера датчиков.


```C++
// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}
```



После успешного получения указателя на [**исенсорманажер**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)можно получить датчики по категории, типу или идентификатору. При получении датчиков по типу или категории вы получаете указатель на интерфейс [**исенсорколлектион**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) , который содержит все доступные датчики, принадлежащие запрошенной категории или типу. Если вы получаете датчик по его ИДЕНТИФИКАТОРу, вы получаете указатель на интерфейс [**исенсор**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) , который представляет запрошенный уникальный датчик.

В следующем примере кода извлекается коллекция датчиков, принадлежащих категории с названием \_ \_ Категория датчика \_ \_ время. Затем код извлекает первый датчик в коллекции по его индексу.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByCategory(SAMPLE_SENSOR_CATEGORY_DATE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested category.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Обратите внимание, что вы можете получить все доступные датчики, используя \_ категорию датчика \_ все.

Аналогичным образом можно получить датчики определенного типа.

В следующем примере кода извлекается коллекция датчиков типа с именем образец \_ типа датчика \_ \_ время. Затем код извлекает первый датчик в коллекции по его индексу.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested type.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Чтобы получить датчик по его ИДЕНТИФИКАТОРу, необходимо узнать уникальный идентификатор датчика. Датчики обычно создают этот идентификатор при первом подключении, чтобы вы определяли несколько датчиков одной и той же марки и модели. Это означает, что вы, вероятно, не будете заранее знакомы с ИДЕНТИФИКАТОРом датчика. Однако если вы сохранили копию определенного идентификатора датчика, полученного ранее, например, вызвав [**исенсор:: GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), вам может потребоваться снова получить тот же датчик.

В следующем примере кода показано, как получить датчик с помощью его идентификатора.


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



Можно также получить датчики, когда они станут доступны, получив событие от диспетчера датчиков. Дополнительные сведения см. в разделе [**исенсорманажер:: сетевентсинк**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Исенсорманажеревентс:: Онсенсорентер**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
