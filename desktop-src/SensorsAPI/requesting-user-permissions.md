---
description: В этом разделе описывается, как запросить у пользователя разрешения на использование датчиков. Общие сведения о разрешениях в API датчика см. в разделе Управление разрешениями пользователей.
ms.assetid: e43ad497-86f1-4804-a67a-0aeb56b80d7f
title: Запрос разрешений пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e103426388d2db49bb5a8fb01d3370207ec49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540898"
---
# <a name="requesting-user-permissions"></a><span data-ttu-id="f3c5b-104">Запрос разрешений пользователя</span><span class="sxs-lookup"><span data-stu-id="f3c5b-104">Requesting User Permissions</span></span>

<span data-ttu-id="f3c5b-105">В этом разделе описывается, как запросить у пользователя разрешения на использование датчиков.</span><span class="sxs-lookup"><span data-stu-id="f3c5b-105">This topic describes how to request permissions from the user to use sensors.</span></span> <span data-ttu-id="f3c5b-106">Общие сведения о разрешениях в API датчика см. в разделе [Управление разрешениями пользователей](managing-user-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="f3c5b-106">For background information about permissions in the Sensor API, see [Managing User Permissions](managing-user-permissions.md).</span></span>

<span data-ttu-id="f3c5b-107">В следующих примерах показаны некоторые распространенные сценариаус, в которых можно запросить разрешения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f3c5b-107">The following examples illustrate some of the common scenarious where you can choose to request user permissions.</span></span>

<span data-ttu-id="f3c5b-108">В следующем примере кода просто запрашиваются разрешения для всех датчиков, полученных от диспетчера датчиков, по типу с помощью асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="f3c5b-108">The following example code simply requests permissions for all sensors retrieved from the sensor manager, by type, using an asynchronous method call.</span></span> <span data-ttu-id="f3c5b-109">Платформа откроет диалоговое окно, в котором пользователю будет предложено только включить датчики, которые еще не включены.</span><span class="sxs-lookup"><span data-stu-id="f3c5b-109">The platform will open a dialog box to prompt the user only to enable sensors that are not already enabled.</span></span> <span data-ttu-id="f3c5b-110">Чтобы определить, включил ли пользователь какие либо датчики в этом случае, необходимо выполнить обработку события [**исенсоревентс:: онстатечанжед**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) .</span><span class="sxs-lookup"><span data-stu-id="f3c5b-110">To determine whether the user enabled any sensors in this case, you must handle the [**ISensorEvents::OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) event.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);

if(SUCCEEDED(hr))
{
    // Request permissions for all sensors
    // in the collection.
    hr = pSensorManager->RequestPermissions(0, pSensorColl, FALSE);
}

```



<span data-ttu-id="f3c5b-111">Вы можете проверить состояние датчика в синхронном режиме, прежде чем пытаться получить данные.</span><span class="sxs-lookup"><span data-stu-id="f3c5b-111">You can choose to test the sensor state synchronously before attempting to retrieve data.</span></span> <span data-ttu-id="f3c5b-112">Этот метод показан в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f3c5b-112">The following example code demonstrates this technique.</span></span>


```C++
if(SUCCEEDED(hr))
{
   // Check the current sensor state.
   SensorState state = SENSOR_STATE_NOT_AVAILABLE;

   hr = pSensor->GetState(&state);

   if(SUCCEEDED(hr))
   {
       if(state == SENSOR_STATE_ACCESS_DENIED)
       {
           wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
           hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

           if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
              hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
           {
               wprintf_s(L"\nYou have previously denied access to this sensor.\n");
               wprintf_s(L"Please use the Location and Other Sensors control panel\n");
               wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
           }
       }
   }
}

if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
```



<span data-ttu-id="f3c5b-113">В следующем примере кода пользователю предлагается разрешение датчика, если попытка извлечь отчет данных с определенного датчика завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f3c5b-113">The following example code prompts the user for sensor permissions if an attempt to retrieve a data report from a particular sensor fails.</span></span>


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);

    if(E_ACCESSDENIED == hr)
    {
       wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
       hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

       if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
          hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
       {
           wprintf_s(L"\nYou have previously denied access to this sensor.\n");
           wprintf_s(L"Please use the Location and Other Sensors control panel\n");
           wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
       }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="f3c5b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f3c5b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c5b-115">**исенсорманажер**</span><span class="sxs-lookup"><span data-stu-id="f3c5b-115">**ISensorManager**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[<span data-ttu-id="f3c5b-116">Управление разрешениями пользователей</span><span class="sxs-lookup"><span data-stu-id="f3c5b-116">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> </dl>

 

 
