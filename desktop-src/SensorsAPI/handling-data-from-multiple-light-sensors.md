---
description: Использование данных освещения
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Использование данных освещения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ccf1c032b4100174afd6073d8c43db27bce3892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664094"
---
# <a name="using-light-sensor-data"></a><span data-ttu-id="b8b74-103">Использование данных освещения</span><span class="sxs-lookup"><span data-stu-id="b8b74-103">Using Light Sensor Data</span></span>

<span data-ttu-id="b8b74-104">Существует два рекомендуемых способа интерпретации и использования данных Lux, поступающих от датчиков внешнего освещения.</span><span class="sxs-lookup"><span data-stu-id="b8b74-104">There are two recommended ways of interpreting and using lux data that comes from ambient light sensors.</span></span>

-   <span data-ttu-id="b8b74-105">Примените преобразование к данным, чтобы нормализованный уровень освещения можно было использовать в прямом пропорции в отношении поведения программы или взаимодействий.</span><span class="sxs-lookup"><span data-stu-id="b8b74-105">Apply a transform to the data so that the normalized light level can be used in direct proportion to program behaviors or interactions.</span></span> <span data-ttu-id="b8b74-106">Например, можно изменить размер кнопки в программе в прямом пропорции на Нормализованные данные (или диапазон нормализованных данных, соответствующий туризм, например).</span><span class="sxs-lookup"><span data-stu-id="b8b74-106">An example would be to vary the size of a button in your program in direct proportion to the normalized data (or a range of the normalized data, corresponding to outdoors, for example).</span></span> <span data-ttu-id="b8b74-107">Такой подход обеспечивает оптимальную реализацию.</span><span class="sxs-lookup"><span data-stu-id="b8b74-107">This approach gives the optimal implementation.</span></span>
-   <span data-ttu-id="b8b74-108">Разработайте с диапазонами данных Lux и сопоставьте поведение программы и реакции на верхние и нижние пороговые значения этих диапазонов данных Lux.</span><span class="sxs-lookup"><span data-stu-id="b8b74-108">Deal with ranges of lux data, and map program behaviors and reactions to the upper and lower thresholds of these ranges of lux data.</span></span> <span data-ttu-id="b8b74-109">Это простой способ реагирования на условия освещения и может не дать оптимального пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b8b74-109">This is a simple way to respond to lighting conditions and may not yield the optimal user experience.</span></span> <span data-ttu-id="b8b74-110">Однако этот подход работает нормально, если плавные переходы нецелесообразны.</span><span class="sxs-lookup"><span data-stu-id="b8b74-110">However, this approach works fine if smooth transitions are not feasible.</span></span>

## <a name="handling-data-from-multiple-light-sensors"></a><span data-ttu-id="b8b74-111">Обработка данных из нескольких датчиков освещения</span><span class="sxs-lookup"><span data-stu-id="b8b74-111">Handling Data from Multiple Light Sensors</span></span>

<span data-ttu-id="b8b74-112">Чтобы получить наиболее точную аппроксимацию текущих условий освещения, можно использовать данные из нескольких внешних датчиков освещения.</span><span class="sxs-lookup"><span data-stu-id="b8b74-112">To produce the most accurate approximation of the current lighting conditions, you can use data from multiple ambient light sensors.</span></span> <span data-ttu-id="b8b74-113">Так как датчики окружающей среды могут частично или полностью закрываться тенями или объектами, охватывающими датчик, несколько датчиков, разоставляющих несколько расстояний, могут обеспечить гораздо лучшую аппроксимацию текущих условий освещения, чем один датчик.</span><span class="sxs-lookup"><span data-stu-id="b8b74-113">Because ambient light sensors can be partly or fully obscured by shadows or objects that cover the sensor, multiple sensors placed some distance apart can provide a much better approximation of the current lighting conditions than a single sensor.</span></span>

<span data-ttu-id="b8b74-114">Чтобы контролировать данные, поступающие из нескольких датчиков, можно использовать следующие два метода:</span><span class="sxs-lookup"><span data-stu-id="b8b74-114">To keep track of the data coming from multiple sensors, you can use the following two techniques:</span></span>

-   <span data-ttu-id="b8b74-115">Для каждого из этих считываний можно хранить самые последние значения данных для каждого датчика окружающей среды, а также отметку времени из отчета с данными датчика.</span><span class="sxs-lookup"><span data-stu-id="b8b74-115">The most recent data value for each ambient light sensor can be retained, along with the time stamp from the sensor data report for each of these readings.</span></span> <span data-ttu-id="b8b74-116">Последняя [**исенсордатарепорт**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) , полученная для каждого считывания датчика, может быть сохранена и может предоставлять оба значения для последующего обращения.</span><span class="sxs-lookup"><span data-stu-id="b8b74-116">The last [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) received for each sensor reading could be retained and could provide both values for later reference.</span></span> <span data-ttu-id="b8b74-117">Ссылаясь на метку времени для каждого отчета с данными датчика, можно управлять данными на основе их возраста.</span><span class="sxs-lookup"><span data-stu-id="b8b74-117">By referring to the time stamp for each sensor data report, the data can be managed based on its age.</span></span> <span data-ttu-id="b8b74-118">Например, если данные более 2 секунд устарели, их можно опустить.</span><span class="sxs-lookup"><span data-stu-id="b8b74-118">For example, if the data is more than 2 seconds old, it could be omitted.</span></span> <span data-ttu-id="b8b74-119">В зависимости от более новых значений данных датчика можно использовать самый большой способ чтения, так как соответствующий датчик предположительно не будет скрываться.</span><span class="sxs-lookup"><span data-stu-id="b8b74-119">Based on the newer sensor data values, the highest reading could be used because the corresponding sensor would be presumed not to be obscured.</span></span>
-   <span data-ttu-id="b8b74-120">Вы можете использовать Последнее значение датчика внешнего освещения.</span><span class="sxs-lookup"><span data-stu-id="b8b74-120">You can use the last ambient light sensor value reported.</span></span> <span data-ttu-id="b8b74-121">Эта реализация не будет оптимальной, так как значения из нескольких датчиков не сравниваются друг с другом, чтобы получить наиболее точный результат.</span><span class="sxs-lookup"><span data-stu-id="b8b74-121">This implementation would not be optimal because the values from multiple sensors are not compared to one another to obtain the most accurate result.</span></span> <span data-ttu-id="b8b74-122">Мы не рекомендуем использовать этот метод.</span><span class="sxs-lookup"><span data-stu-id="b8b74-122">We do not recommend this method.</span></span>

## <a name="example-code"></a><span data-ttu-id="b8b74-123">Пример кода</span><span class="sxs-lookup"><span data-stu-id="b8b74-123">Example Code</span></span>

<span data-ttu-id="b8b74-124">В следующем примере кода показана реализация для события [**ондатаупдатед**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) .</span><span class="sxs-lookup"><span data-stu-id="b8b74-124">The following example code shows an implementation for the [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="b8b74-125">Обработчик событий вызывает вспомогательную функцию с именем **упдатеуи**, которая изменяет пользовательский интерфейс на основе значения Lux.</span><span class="sxs-lookup"><span data-stu-id="b8b74-125">The event handler calls a helper function, named **UpdateUI**, that changes the user interface based on the lux value.</span></span> <span data-ttu-id="b8b74-126">Написание реализации Упдатеуи в вашей области.</span><span class="sxs-lookup"><span data-stu-id="b8b74-126">Writing the implementation of UpdateUI is up to you.</span></span>


```C++
// Override of ISensorEvents::OnDataUpdated
// Part of an event sink implementation for ISensorEvents
STDMETHODIMP CALSEventSink::OnDataUpdated(
    ISensor* pSensor, 
    ISensorDataReport* pNewData)
{
    HRESULT hr = S_OK;
   
    if(pSensor == NULL ||
       pNewData == NULL)
    {
         return E_POINTER;
    }

    // Declare and initialize the PROPVARIANT
    PROPVARIANT lightLevel;
    PropVariantInit(&lightLevel);

    // Get the sensor reading from the ISensorDataReport object
    hr = pNewData->GetSensorValue(
        SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX, 
        &lightLevel);

    if(SUCCEEDED(hr))
    {
        if(lightlevel.vt == VT_R4)
        {
            // Extract the float value from the PROPVARIANT object
            float luxValue = lightLevel.fltVal;

            // Normalize the light sensor data
            double lightNormalized = ::log10(luxValue) / 5.0;

            // Handle UI changes based on the normalized LUX data
            // which ranges from 0.0 - 1.0 for a lux range of 
            // 0 lux to 100,000 lux. 
            UpdateUI(lightNormalized);
        }
    }

    // Release the variant.     
    PropVariantClear(&lightLevel);

    return hr;
}
```



 

 
