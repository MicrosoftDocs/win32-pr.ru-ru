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
# <a name="using-logical-sensors"></a><span data-ttu-id="2fe9a-103">Использование логических датчиков</span><span class="sxs-lookup"><span data-stu-id="2fe9a-103">Using Logical Sensors</span></span>

<span data-ttu-id="2fe9a-104">Чтобы создать экземпляр узла устройства для логического датчика или повторно подключиться к существующему узлу логического датчика, приложение или служба должны вызвать [**илогикалсенсорманажер:: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2fe9a-104">To instantiate a device node for a logical sensor, or to reconnect to an existing logical sensor device node, an application or service must call [**ILogicalSensorManager::Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span> <span data-ttu-id="2fe9a-105">Для параметра *ппропертисторе* этого метода требуется указатель на интерфейс [Ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) , содержащий идентификаторы для драйверов датчиков, к которым необходимо подключиться.</span><span class="sxs-lookup"><span data-stu-id="2fe9a-105">The *pPropertyStore* parameter for this method requires a pointer to an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface that contains the IDs for the sensor drivers to connect to.</span></span> <span data-ttu-id="2fe9a-106">Это означает, что необходимо создать хранилище свойств и добавить эти данные в хранилище перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="2fe9a-106">This means that you must create a property store and add this data to the store before calling this method.</span></span>

### <a name="connecting-to-the-logical-sensor"></a><span data-ttu-id="2fe9a-107">Подключение к логическому датчику</span><span class="sxs-lookup"><span data-stu-id="2fe9a-107">Connecting to the Logical Sensor</span></span>

<span data-ttu-id="2fe9a-108">Для подключения к логическому датчику необходимо указать по крайней мере идентификатор оборудования, как определено в INF-файле драйвера датчика, и логический **идентификатор GUID** , определяющий датчик.</span><span class="sxs-lookup"><span data-stu-id="2fe9a-108">To connect to a logical sensor, you must provide, at a minimum, a hardware ID, as defined in the sensor driver's .inf file, and a logical **GUID** that identifies the sensor.</span></span> <span data-ttu-id="2fe9a-109">Платформа использует этот **идентификатор GUID** для обнаружения датчика, если вы решили отключиться от узла устройства датчика или удалить его.</span><span class="sxs-lookup"><span data-stu-id="2fe9a-109">The platform uses this **GUID** to identify the sensor when you choose to disconnect from, or uninstall, the sensor device node.</span></span>

<span data-ttu-id="2fe9a-110">В следующем примере кода создается вспомогательный метод, который подключается к указанному логическому датчику.</span><span class="sxs-lookup"><span data-stu-id="2fe9a-110">The following example code creates a helper method that connects to a specified logical sensor.</span></span> <span data-ttu-id="2fe9a-111">Параметры метода получают идентификатор оборудования датчика и уникальный **идентификатор GUID** для идентификации датчика.</span><span class="sxs-lookup"><span data-stu-id="2fe9a-111">The method parameters receive the sensor hardware ID and a unique **GUID** to identify the sensor.</span></span>


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



### <a name="disconnecting-from-a-logical-sensor"></a><span data-ttu-id="2fe9a-112">Отключение от логического датчика</span><span class="sxs-lookup"><span data-stu-id="2fe9a-112">Disconnecting from a Logical Sensor</span></span>

<span data-ttu-id="2fe9a-113">Для отключения от логического датчика необходимо указать тот же логический идентификатор, который использовался при вызове [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2fe9a-113">To disconnect from a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="2fe9a-114">В следующем примере кода создается вспомогательная функция, которая отключается от логического датчика.</span><span class="sxs-lookup"><span data-stu-id="2fe9a-114">The following example code creates a helper function that disconnects from a logical sensor.</span></span>


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



### <a name="uninstalling-a-logical-sensor"></a><span data-ttu-id="2fe9a-115">Удаление логического датчика</span><span class="sxs-lookup"><span data-stu-id="2fe9a-115">Uninstalling a Logical Sensor</span></span>

<span data-ttu-id="2fe9a-116">Чтобы удалить логический датчик, необходимо указать тот же логический идентификатор, который использовался при вызове [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2fe9a-116">To uninstall a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="2fe9a-117">В следующем примере кода создается вспомогательная функция, которая удаляет логический датчик.</span><span class="sxs-lookup"><span data-stu-id="2fe9a-117">The following example code creates a helper function that uninstalls a logical sensor.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2fe9a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="2fe9a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fe9a-119">О логических датчиках</span><span class="sxs-lookup"><span data-stu-id="2fe9a-119">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> </dl>

 

 
