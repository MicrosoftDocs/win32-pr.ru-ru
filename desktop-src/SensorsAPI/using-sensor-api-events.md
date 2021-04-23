---
description: API датчика предоставляет уведомления о событиях через интерфейсы обратного вызова.
ms.assetid: 0c396d54-cb2e-4b07-999f-3f4001db2a02
title: Использование событий API датчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54fcb14138c1b20470a2b716e5cce86235c3102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998878"
---
# <a name="using-sensor-api-events"></a><span data-ttu-id="d029d-103">Использование событий API датчика</span><span class="sxs-lookup"><span data-stu-id="d029d-103">Using Sensor API Events</span></span>

<span data-ttu-id="d029d-104">API датчика предоставляет уведомления о событиях через интерфейсы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d029d-104">The Sensor API provides event notifications through callback interfaces.</span></span>

<span data-ttu-id="d029d-105">Чтобы получить нотфикатионс событий, программа должна реализовать необходимые интерфейсы обратного вызова COM.</span><span class="sxs-lookup"><span data-stu-id="d029d-105">To receive event notfications, your program must implement the required COM callback interfaces.</span></span> <span data-ttu-id="d029d-106">Для получения событий от датчиков необходимо реализовать [**исенсоревентс**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="d029d-106">To receive events from sensors, you must implement [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="d029d-107">Чтобы получить события от диспетчера датчиков, необходимо реализовать [**исенсорманажеревентс**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="d029d-107">To receive events from the sensor manager, you must implement [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span>

<span data-ttu-id="d029d-108">В следующем примере кода создается класс, реализующий [**исенсоревентс**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="d029d-108">The following example code creates a class that implements [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span>


```C++
class CMyEvents : public ISensorEvents
{
public:

    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        if (ppv == NULL)
        {
            return E_POINTER;
        }
        if (iid == __uuidof(IUnknown))
        {
            *ppv = static_cast<IUnknown*>(this);
        }
        else if (iid == __uuidof(ISensorEvents))
        {
            *ppv = static_cast<ISensorEvents*>(this);
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
        AddRef();
        return S_OK;
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef); 
    }

    STDMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    //
    // ISensorEvents methods.
    //

    STDMETHODIMP OnEvent(
            ISensor *pSensor,
            REFGUID eventID,
            IPortableDeviceValues *pEventData)
    {
        HRESULT hr = S_OK;

        // Handle custom events here.

        return hr;
    }

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

    STDMETHODIMP OnLeave(
            REFSENSOR_ID sensorID)
    {
        HRESULT hr = S_OK;

        // Peform any housekeeping tasks for the sensor that is leaving.
        // For example, if you have maintained a reference to the sensor,
        // release it now and set the pointer to NULL.

        return hr;
    }

    STDMETHODIMP OnStateChanged(
            ISensor* pSensor,
            SensorState state)
    {
        HRESULT hr = S_OK;

        if(NULL == pSensor)
        {
            return E_INVALIDARG;
        }


        if(state == SENSOR_STATE_READY)
        {
            wprintf_s(L"\nTime sensor is now ready.");
        }
        else if(state == SENSOR_STATE_ACCESS_DENIED)
        {
            wprintf_s(L"\nNo permission for the time sensor.\n");
            wprintf_s(L"Enable the sensor in the control panel.\n");
        }
  

        return hr;
    }

    private:
        long m_cRef;

};

```



<span data-ttu-id="d029d-109">После реализации интерфейса обратного вызова можно предоставить определенный датчик с указателем на экземпляр класса обратного вызова, чтобы начать получать уведомления о событиях от датчика.</span><span class="sxs-lookup"><span data-stu-id="d029d-109">After implementing the callback interface, you can provide a particular sensor with a pointer to an instance of your callback class to start receiving event notifications from the sensor.</span></span>

<span data-ttu-id="d029d-110">В следующем примере кода создается экземпляр класса обратного вызова, а затем из датчика запрашиваются нотифкатионс событий.</span><span class="sxs-lookup"><span data-stu-id="d029d-110">The following example code creates an instance of the callback class, and then requests event notifcations from a sensor.</span></span>


```C++
CMyEvents* pEventClass = NULL;
ISensorEvents* pMyEvents = NULL;

if(SUCCEEDED(hr))
{
    // Create an instance of the event class.
    pEventClass = new(std::nothrow) CMyEvents();        
}

if(SUCCEEDED(hr))
{
    // Retrieve the pointer to the callback interface.
    hr = pEventClass->QueryInterface(IID_PPV_ARGS(&pMyEvents));
}

if(SUCCEEDED(hr))
{
    // Start receiving events.
    hr = pSensor->SetEventSink(pMyEvents);
} 

```



<span data-ttu-id="d029d-111">Можно написать аналогичный код для получения событий от диспетчера датчиков.</span><span class="sxs-lookup"><span data-stu-id="d029d-111">You can write similar code to receive events from the sensor manager.</span></span>

<span data-ttu-id="d029d-112">В следующем примере кода показано, как отключить получение уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="d029d-112">The following example code shows how to stop receiving event notifications.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = pSensor->SetEventSink(NULL);
}
```



## <a name="requesting-a-report-interval"></a><span data-ttu-id="d029d-113">Запрос интервала отчета</span><span class="sxs-lookup"><span data-stu-id="d029d-113">Requesting a Report Interval</span></span>

<span data-ttu-id="d029d-114">Вы можете предложить значение для того, как часто приложения отменено получает события, обновленные данными.</span><span class="sxs-lookup"><span data-stu-id="d029d-114">You can suggest a value for how frequently your applicaton receives data-updated events.</span></span> <span data-ttu-id="d029d-115">Однако датчики не являются обязательными для предоставления событий в определенный промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="d029d-115">However, sensors are not required to provide events at any particular interval.</span></span> <span data-ttu-id="d029d-116">Следует иметь в виду, что предлагаемое значение может не совпадать с фактическим интервалом отчета, который датчик использует для вызова событий.</span><span class="sxs-lookup"><span data-stu-id="d029d-116">You should be aware that your suggested value might not match the actual report interval the sensor uses to raise events.</span></span> <span data-ttu-id="d029d-117">Чтобы узнать фактический интервал отчетов, извлеките значение свойства датчика \_ \_ текущего \_ \_ интервала отчета, как описано в разделе [Получение и Настройка свойств датчика](setting-and-retrieving-sensor-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d029d-117">To know the actual report interval, retrieve the value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property, as described in [Retrieving and Setting Sensor Properties](setting-and-retrieving-sensor-properties.md).</span></span>

<span data-ttu-id="d029d-118">В следующем примере кода создается вспомогательная функция, которая запрашивает новое значение \_ \_ \_ свойства интервала текущего отчета для свойства датчика \_ .</span><span class="sxs-lookup"><span data-stu-id="d029d-118">The following example code creates a helper function that requests a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="d029d-119">Функция принимает указатель на датчик, для которого задается свойство, и значение **ulong** , указывающее, какой интервал времени должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="d029d-119">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d029d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d029d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d029d-121">Сведения о событиях API датчика</span><span class="sxs-lookup"><span data-stu-id="d029d-121">About Sensor API Events</span></span>](about-sensor-events.md)
</dt> </dl>

 

 



