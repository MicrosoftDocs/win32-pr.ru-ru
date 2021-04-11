---
description: Использование логических датчиков
ms.assetid: 97f4c44e-27dd-4f2a-b987-060bb2d9bc00
title: Использование логических датчиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0493cfe8ff3a489e926792f9a101eb5d9db6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144383"
---
# <a name="using-logical-sensors"></a>Использование логических датчиков

Чтобы создать экземпляр узла устройства для логического датчика или повторно подключиться к существующему узлу логического датчика, приложение или служба должны вызвать [**илогикалсенсорманажер:: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)). Для параметра *ппропертисторе* этого метода требуется указатель на интерфейс [Ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) , содержащий идентификаторы для драйверов датчиков, к которым необходимо подключиться. Это означает, что необходимо создать хранилище свойств и добавить эти данные в хранилище перед вызовом этого метода.

### <a name="connecting-to-the-logical-sensor"></a>Подключение к логическому датчику

Для подключения к логическому датчику необходимо указать по крайней мере идентификатор оборудования, как определено в INF-файле драйвера датчика, и логический **идентификатор GUID** , определяющий датчик. Платформа использует этот **идентификатор GUID** для обнаружения датчика, если вы решили отключиться от узла устройства датчика или удалить его.

В следующем примере кода создается вспомогательный метод, который подключается к указанному логическому датчику. Параметры метода получают идентификатор оборудования датчика и уникальный **идентификатор GUID** для идентификации датчика.


```C++
HRESULT ConnectToLogicalSensor(PCWSTR* wszHardwareID, GUID guidLogicalID)
{
    HRESULT hr = S_OK;
    
    ILogicalSensorManager* pLSM = NULL;
    IPropertyStore* pStore = NULL;
    PROPVARIANT pv = {};

    // Create the property store.
    hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pStore));

    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    // Fill in the values.
    if(SUCCEEDED(hr))
    {
        hr = InitPropVariantFromStringVector(wszHardwareID, 1, &pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_HardwareIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_CompatibleIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        // Connect to the logical sensor.
        hr = pLSM->Connect(guidLogicalID, pStore);
    }

    SafeRelease(&pStore);
    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="disconnecting-from-a-logical-sensor"></a>Отключение от логического датчика

Для отключения от логического датчика необходимо указать тот же логический идентификатор, который использовался при вызове [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

В следующем примере кода создается вспомогательная функция, которая отключается от логического датчика.


```C++
HRESULT DisconnectFromLogicalSensor(GUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM = NULL;
 
    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    if(SUCCEEDED(hr))
    {
        hr = pLSM->Disconnect(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="uninstalling-a-logical-sensor"></a>Удаление логического датчика

Чтобы удалить логический датчик, необходимо указать тот же логический идентификатор, который использовался при вызове [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

В следующем примере кода создается вспомогательная функция, которая удаляет логический датчик.


```C++
HRESULT UninstallLogicalSensor(REFGUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM;
 
    // Create the logical sensor manager.
    hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_PPV_ARGS(&pLSM));
 
    if(SUCCEEDED(hr))
    {
        hr = pLSM->Uninstall(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[О логических датчиках](about-logical-sensors.md)
</dt> </dl>

 

 
