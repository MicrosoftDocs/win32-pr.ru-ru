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
# <a name="retrieving-a-sensor-object"></a><span data-ttu-id="96312-105">Получение объекта датчика</span><span class="sxs-lookup"><span data-stu-id="96312-105">Retrieving a Sensor Object</span></span>

<span data-ttu-id="96312-106">Для получения объекта датчика используется интерфейс [**исенсорманажер**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) .</span><span class="sxs-lookup"><span data-stu-id="96312-106">To retrieve a sensor object, you use the [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) interface.</span></span> <span data-ttu-id="96312-107">Этот интерфейс можно считать корневым интерфейсом для API датчика.</span><span class="sxs-lookup"><span data-stu-id="96312-107">You can think of this interface as the root interface for the Sensor API.</span></span> <span data-ttu-id="96312-108">Чтобы использовать **исенсорманажер**, необходимо сначала вызвать метод COM **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="96312-108">To use **ISensorManager**, you must first call the COM **CoCreateInstance** method.</span></span>

<span data-ttu-id="96312-109">В следующем примере кода создается экземпляр диспетчера датчиков.</span><span class="sxs-lookup"><span data-stu-id="96312-109">The following example code creates an instance of the sensor manager.</span></span>


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



<span data-ttu-id="96312-110">После успешного получения указателя на [**исенсорманажер**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)можно получить датчики по категории, типу или идентификатору.</span><span class="sxs-lookup"><span data-stu-id="96312-110">After successfully retrieving a pointer to [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), you can retrieve sensors by category, type, or ID.</span></span> <span data-ttu-id="96312-111">При получении датчиков по типу или категории вы получаете указатель на интерфейс [**исенсорколлектион**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) , который содержит все доступные датчики, принадлежащие запрошенной категории или типу.</span><span class="sxs-lookup"><span data-stu-id="96312-111">If you retrieve sensors by type or category, you receive a pointer to an [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) interface that contains all the available sensors that belong to the requested category or type.</span></span> <span data-ttu-id="96312-112">Если вы получаете датчик по его ИДЕНТИФИКАТОРу, вы получаете указатель на интерфейс [**исенсор**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) , который представляет запрошенный уникальный датчик.</span><span class="sxs-lookup"><span data-stu-id="96312-112">If you retrieve a sensor by its ID, you receive a pointer to an [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface that represents the unique sensor you requested.</span></span>

<span data-ttu-id="96312-113">В следующем примере кода извлекается коллекция датчиков, принадлежащих категории с названием \_ \_ Категория датчика \_ \_ время.</span><span class="sxs-lookup"><span data-stu-id="96312-113">The following example code retrieves a collection of sensors that belong to the category named SAMPLE\_SENSOR\_CATEGORY\_DATE\_TIME.</span></span> <span data-ttu-id="96312-114">Затем код извлекает первый датчик в коллекции по его индексу.</span><span class="sxs-lookup"><span data-stu-id="96312-114">The code then retrieves the first sensor in the collection by its index.</span></span>


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



<span data-ttu-id="96312-115">Обратите внимание, что вы можете получить все доступные датчики, используя \_ категорию датчика \_ все.</span><span class="sxs-lookup"><span data-stu-id="96312-115">Note that you can retrieve all of the available sensors by using SENSOR\_CATEGORY\_ALL.</span></span>

<span data-ttu-id="96312-116">Аналогичным образом можно получить датчики определенного типа.</span><span class="sxs-lookup"><span data-stu-id="96312-116">In a similar way, you can retrieve sensors of a particular type.</span></span>

<span data-ttu-id="96312-117">В следующем примере кода извлекается коллекция датчиков типа с именем образец \_ типа датчика \_ \_ время.</span><span class="sxs-lookup"><span data-stu-id="96312-117">The following example code retrieves a collection of sensors of the type named SAMPLE\_SENSOR\_TYPE\_TIME.</span></span> <span data-ttu-id="96312-118">Затем код извлекает первый датчик в коллекции по его индексу.</span><span class="sxs-lookup"><span data-stu-id="96312-118">The code then retrieves the first sensor in the collection by its index.</span></span>


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



<span data-ttu-id="96312-119">Чтобы получить датчик по его ИДЕНТИФИКАТОРу, необходимо узнать уникальный идентификатор датчика.</span><span class="sxs-lookup"><span data-stu-id="96312-119">To retrieve a sensor by its ID, you must know the unique ID for the sensor.</span></span> <span data-ttu-id="96312-120">Датчики обычно создают этот идентификатор при первом подключении, чтобы вы определяли несколько датчиков одной и той же марки и модели.</span><span class="sxs-lookup"><span data-stu-id="96312-120">Sensors usually generate this ID when first connected to enable you to identify multiple sensors of the same make and model.</span></span> <span data-ttu-id="96312-121">Это означает, что вы, вероятно, не будете заранее знакомы с ИДЕНТИФИКАТОРом датчика.</span><span class="sxs-lookup"><span data-stu-id="96312-121">This means that you probably will not know the sensor ID in advance.</span></span> <span data-ttu-id="96312-122">Однако если вы сохранили копию определенного идентификатора датчика, полученного ранее, например, вызвав [**исенсор:: GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), вам может потребоваться снова получить тот же датчик.</span><span class="sxs-lookup"><span data-stu-id="96312-122">However, if you have stored a copy of a particular sensor ID that you previously retrieved, for example by calling [**ISensor::GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), you may want to retrieve the same sensor again.</span></span>

<span data-ttu-id="96312-123">В следующем примере кода показано, как получить датчик с помощью его идентификатора.</span><span class="sxs-lookup"><span data-stu-id="96312-123">The following example code shows how to retrieve a sensor by using its ID.</span></span>


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



<span data-ttu-id="96312-124">Можно также получить датчики, когда они станут доступны, получив событие от диспетчера датчиков.</span><span class="sxs-lookup"><span data-stu-id="96312-124">You can also retrieve sensors when they become available by receiving an event from the sensor manager.</span></span> <span data-ttu-id="96312-125">Дополнительные сведения см. в разделе [**исенсорманажер:: сетевентсинк**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span><span class="sxs-lookup"><span data-stu-id="96312-125">For more information, see [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96312-126">См. также</span><span class="sxs-lookup"><span data-stu-id="96312-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96312-127">**Исенсорманажеревентс:: Онсенсорентер**</span><span class="sxs-lookup"><span data-stu-id="96312-127">**ISensorManagerEvents::OnSensorEnter**</span></span>](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
