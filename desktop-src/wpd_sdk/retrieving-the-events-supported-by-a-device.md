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
# <a name="retrieving-the-events-supported-by-a-device"></a>Получение событий, поддерживаемых устройством

Некоторые драйверы WPD поддерживают уведомления о событиях. Это означает, что приложение может зарегистрироваться в драйвере, чтобы получить уведомление при выполнении определенного действия. Например, приложение может зарегистрироваться, чтобы получить уведомление при добавлении или удалении объекта.

Существует десять предопределенных событий, которые может отслеживать приложение. Они описаны в следующей таблице.



| Событие                       | Описание                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Возможности устройства обновлены | Происходит при изменении возможностей устройства.                                                                                      |
| Устройство удалено              | Происходит при отсоединении устройства.                                                                                                   |
| сброс настроек устройства;                | Происходит при сбросе устройства.                                                                                                 |
| Объект добавлен                | Происходит после того, как новый объект станет доступным на устройстве.                                                                             |
| Объект удален              | Происходит после удаления объекта с устройства.                                                                               |
| Запрошено перемещение объектов   | Указывает, что был выполнен запрос на перемещение объекта.                                                                          |
| Объект обновлен              | Происходит после обновления объекта или его дочерних элементов. (Подключенные клиенты должны затем обновить представление заданного объекта.) |
| Выполняется форматирование хранилища  | Происходит при форматировании хранилища устройства.                                                                                     |



 

Список констант, связанных с этими событиями, см. в разделе [константы событий](event-constants.md) .

Функция Листсуппортедевентс в модуле Девицекапабилитиес. cpp демонстрирует получение событий, поддерживаемых данным устройством.

Приложение может извлекать идентификаторы для событий, поддерживаемых устройством, с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                                      | Описание                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Интерфейс Ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Предоставляет доступ к методам получения поддерживаемых событий. |
| [**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Используется для перечисления и хранения данных функциональной категории.     |



 

Первая задача, выполняемая примером приложения, — это извлечение объекта [**ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , который используется для получения событий, поддерживаемых данным устройством.


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



Поддерживаемые события извлекаются путем вызова метода [**ипортабледевицекапабилитиес:: жетсуппортедевентс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) . Этот метод получает коллекцию идентификаторов событий для данного устройства и сохраняет их в объекте [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , на который указывает аргумент певентс.


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



Следующим шагом является получение количества поддерживаемых событий, чтобы приложение может выполнить итерацию по объекту [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) и получить идентификатор для каждого из них.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Константы событий**](event-constants.md)
</dt> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



