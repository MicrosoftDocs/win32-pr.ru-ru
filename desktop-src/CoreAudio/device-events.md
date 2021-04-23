---
description: События устройства
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: События устройства (основные API-интерфейсы для аудиоподсистемы)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655627"
---
# <a name="device-events-core-audio-apis"></a><span data-ttu-id="8d6d8-103">События устройства (основные API-интерфейсы для аудиоподсистемы)</span><span class="sxs-lookup"><span data-stu-id="8d6d8-103">Device Events (Core Audio APIs)</span></span>

<span data-ttu-id="8d6d8-104">Событие устройства уведомляет клиентов об изменении состояния [устройства конечной точки аудио](audio-endpoint-devices.md) в системе.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-104">A device event notifies clients of a change in the status of an [audio endpoint device](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="8d6d8-105">Ниже приведены примеры событий устройств.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-105">The following are examples of device events:</span></span>

-   <span data-ttu-id="8d6d8-106">Пользователь включает или отключает устройство звуковой конечной точки из диспетчер устройств или с помощью панели управления Windows мультимедиа Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-106">The user enables or disables an audio endpoint device from Device Manager or from the Windows multimedia control panel, Mmsys.cpl.</span></span>
-   <span data-ttu-id="8d6d8-107">Пользователь добавляет звуковой адаптер в систему или удаляет звуковой адаптер из системы.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-107">The user adds an audio adapter to the system or removes an audio adapter from the system.</span></span>
-   <span data-ttu-id="8d6d8-108">Пользователь подключает устройство аудио конечных точек к звуковой розетке с обнаружением разъема или удаляет устройство звуковой конечной точки с такого разъема.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-108">The user plugs an audio endpoint device into an audio jack with jack-presence detection, or removes an audio endpoint device from such a jack.</span></span>
-   <span data-ttu-id="8d6d8-109">Пользователь изменяет [роль устройства](device-roles.md) , назначенную устройству.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-109">The user changes the [device role](device-roles.md) that is assigned to a device.</span></span>
-   <span data-ttu-id="8d6d8-110">Значение [Свойства устройства](device-properties.md) изменяется.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-110">The value of a [property of a device](device-properties.md) changes.</span></span>

<span data-ttu-id="8d6d8-111">Добавление или удаление звукового адаптера создает события устройства для всех устройств конечных точек аудио, подключающихся к адаптеру.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-111">The addition or removal of an audio adapter generates device events for all of the audio endpoint devices that connect to the adapter.</span></span> <span data-ttu-id="8d6d8-112">Первые четыре элемента в приведенном выше списке являются примерами изменений состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-112">The first four items in the preceding list are examples of device state changes.</span></span> <span data-ttu-id="8d6d8-113">Дополнительные сведения о состояниях устройств конечных точек звука см. в разделе [Device \_ State \_ xxx константы](device-state-xxx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8d6d8-113">For more information about the device states of audio endpoint devices, see [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).</span></span> <span data-ttu-id="8d6d8-114">Дополнительные сведения об обнаружении устройств с разъемами см. в статье [устройства конечных точек аудио](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="8d6d8-114">For more information about jack-presence detection, see [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="8d6d8-115">Клиент может зарегистрироваться, чтобы получать уведомления при возникновении событий устройства.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-115">A client can register to be notified when device events occur.</span></span> <span data-ttu-id="8d6d8-116">В ответ на эти уведомления клиент может динамически изменить способ использования определенного устройства или выбрать другое устройство для использования в конкретной цели.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-116">In response to these notifications, the client can dynamically change the way that it uses a particular device, or select a different device to use for a particular purpose.</span></span>

<span data-ttu-id="8d6d8-117">Например, если приложение воспроизводит звуковую дорожку через набор динамиков USB, и пользователь отключает динамики от USB-разъема, приложение получает уведомление о событии устройства.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-117">For example, if an application is playing an audio track through a set of USB speakers, and the user disconnects the speakers from the USB connector, the application receives a device-event notification.</span></span> <span data-ttu-id="8d6d8-118">В ответ на событие, если приложение обнаруживает, что набор настольных динамиков подключен к интегрированному звуковому адаптеру на системной плате, приложение может возобновить воспроизведение звуковой дорожки через динамики рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-118">In response to the event, if the application detects that a set of desktop speakers is connected to the integrated audio adapter on the system motherboard, the application can resume playing the audio track through the desktop speakers.</span></span> <span data-ttu-id="8d6d8-119">В этом примере переход от динамиков USB к динамикам настольных компьютеров происходит автоматически, не требуя от пользователя явного перенаправления приложения.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-119">In this example, the transition from USB speakers to desktop speakers occurs automatically, without requiring the user to intervene by explicitly redirecting the application.</span></span>

<span data-ttu-id="8d6d8-120">Чтобы зарегистрироваться для получения уведомлений устройства, клиент вызывает метод [**иммдевицеенумератор:: регистерендпоинтнотификатионкаллбакк**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="8d6d8-120">To register to receive device notifications, a client calls the [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) method.</span></span> <span data-ttu-id="8d6d8-121">Если клиенту больше не требуются уведомления, он отменяет их, вызывая метод [**иммдевицеенумератор:: унрегистерендпоинтнотификатионкаллбакк**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="8d6d8-121">When the client no longer requires notifications, it cancels them by calling the [**IMMDeviceEnumerator::UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) method.</span></span> <span data-ttu-id="8d6d8-122">Оба метода принимают входной параметр с именем *пнотифи*, который является указателем на экземпляр интерфейса [**иммнотификатионклиент**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) .</span><span class="sxs-lookup"><span data-stu-id="8d6d8-122">Both methods take an input parameter, named *pNotify*, that is a pointer to an [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) interface instance.</span></span>

<span data-ttu-id="8d6d8-123">Интерфейс **иммнотификатионклиент** реализуется клиентом.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-123">The **IMMNotificationClient** interface is implemented by a client.</span></span> <span data-ttu-id="8d6d8-124">Интерфейс содержит несколько методов, каждый из которых служит подпрограммы обратного вызова для определенного типа события устройства.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-124">The interface contains several methods, each of which serves as a callback routine for a particular type of device event.</span></span> <span data-ttu-id="8d6d8-125">При возникновении события устройства в конечной точке звука модуль Ммдевице вызывает соответствующий метод в интерфейсе **иммнотификатионклиент** каждого клиента, зарегистрированного для получения уведомлений о событиях устройства.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-125">When a device event occurs in an audio endpoint device, the MMDevice module calls the appropriate method in the **IMMNotificationClient** interface of every client that is currently registered to receive device-event notifications.</span></span> <span data-ttu-id="8d6d8-126">Эти вызовы передают описание события клиентам.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-126">These calls pass a description of the event to the clients.</span></span> <span data-ttu-id="8d6d8-127">Дополнительные сведения см. в разделе [**интерфейс иммнотификатионклиент**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="8d6d8-127">For more information, see [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span>

<span data-ttu-id="8d6d8-128">Клиент, зарегистрированный для получения уведомлений о событиях устройства, будет получать уведомления обо всех типах событий устройств, происходящих во всех конечных устройствах аудио в системе.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-128">A client that is registered to receive device-event notifications will receive notifications of all types of device events that occur in all of the audio endpoint devices in the system.</span></span> <span data-ttu-id="8d6d8-129">Если клиент заинтересован только в определенных типах событий или на определенных устройствах, то методы в его реализации **иммнотификатионклиент** должны соответствующим образом фильтровать события.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-129">If a client is interested only in certain event types or in certain devices, then the methods in its **IMMNotificationClient** implementation should filter the events appropriately.</span></span>

<span data-ttu-id="8d6d8-130">Windows SDK предоставляет примеры, включающие несколько реализаций для [**интерфейса иммнотификатионклиент**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="8d6d8-130">The Windows SDK provides samples that include several implementations for the [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span> <span data-ttu-id="8d6d8-131">Дополнительные сведения см. [в статье примеры пакетов SDK, в которых используются основные API аудио](sdk-samples-that-use-the-core-audio-apis.md).</span><span class="sxs-lookup"><span data-stu-id="8d6d8-131">For more information, see [SDK Samples That Use the Core Audio APIs](sdk-samples-that-use-the-core-audio-apis.md).</span></span>

<span data-ttu-id="8d6d8-132">В следующем примере кода показана возможная реализация интерфейса **иммнотификатионклиент** :</span><span class="sxs-lookup"><span data-stu-id="8d6d8-132">The following code example shows a possible implementation of the **IMMNotificationClient** interface:</span></span>


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



<span data-ttu-id="8d6d8-133">Класс Кммнотификатионклиент в предыдущем примере кода является реализацией интерфейса **иммнотификатионклиент** .</span><span class="sxs-lookup"><span data-stu-id="8d6d8-133">The CMMNotificationClient class in the preceding code example is an implementation of the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="8d6d8-134">Поскольку **иммнотификатионклиент** наследует от **IUnknown**, определение класса содержит реализации методов **IUnknown** , **AddRef**, **Release** и **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-134">Because **IMMNotificationClient** inherits from **IUnknown**, the class definition contains implementations of the **IUnknown** methods **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="8d6d8-135">Остальные открытые методы в определении класса относятся к интерфейсу **иммнотификатионклиент** .</span><span class="sxs-lookup"><span data-stu-id="8d6d8-135">The remaining public methods in the class definition are specific to the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="8d6d8-136">Этими методами являются:</span><span class="sxs-lookup"><span data-stu-id="8d6d8-136">These methods are:</span></span>

-   <span data-ttu-id="8d6d8-137">**Ондефаултдевицечанжед**, который вызывается при изменении пользователем роли устройства конечной точки звука.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-137">**OnDefaultDeviceChanged**, which is called when the user changes the device role of an audio endpoint device.</span></span>
-   <span data-ttu-id="8d6d8-138">**Ондевицеаддед**, который вызывается, когда пользователь добавляет устройство конечной точки аудио в систему.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-138">**OnDeviceAdded**, which is called when the user adds an audio endpoint device to the system.</span></span>
-   <span data-ttu-id="8d6d8-139">**Ондевицеремовед**, который вызывается, когда пользователь удаляет устройство конечной точки аудио из системы.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-139">**OnDeviceRemoved**, which is called when the user removes an audio endpoint device from the system.</span></span>
-   <span data-ttu-id="8d6d8-140">**Ондевицестатечанжед**, который вызывается при изменении состояния устройства для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-140">**OnDeviceStateChanged**, which is called when the device state of an audio endpoint device changes.</span></span> <span data-ttu-id="8d6d8-141">(Дополнительные сведения о состояниях устройств см. в разделе [Device \_ State \_ xxx константы](device-state-xxx-constants.md).)</span><span class="sxs-lookup"><span data-stu-id="8d6d8-141">(For more information about device states, see [DEVICE\_STATE\_ XXX Constants](device-state-xxx-constants.md).)</span></span>
-   <span data-ttu-id="8d6d8-142">**Онпропертивалуечанжед**, который вызывается при изменении значения свойства устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-142">**OnPropertyValueChanged**, which is called when the value of a property of an audio endpoint device changes.</span></span>

<span data-ttu-id="8d6d8-143">Каждый из этих методов принимает входной параметр *пвстрдевицеид*, который является указателем на строку идентификатора конечной точки.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-143">Each of these methods takes an input parameter, *pwstrDeviceId*, that is a pointer to an endpoint ID string.</span></span> <span data-ttu-id="8d6d8-144">Строка определяет устройство аудио конечной точки, в котором произошло событие устройства.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-144">The string identifies the audio endpoint device in which the device event occurred.</span></span>

<span data-ttu-id="8d6d8-145">В предыдущем примере кода \_ принтдевиценаме является частным методом в классе кммнотификатионклиент, который выводит понятное имя устройства.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-145">In the preceding code example, \_PrintDeviceName is a private method in the CMMNotificationClient class that prints the friendly name of the device.</span></span> <span data-ttu-id="8d6d8-146">\_Принтдевиценаме принимает строку идентификатора конечной точки в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-146">\_PrintDeviceName takes the endpoint ID string as an input parameter.</span></span> <span data-ttu-id="8d6d8-147">Он передает строку в метод [**иммдевицеенумератор::**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) GetString.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-147">It passes the string to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="8d6d8-148">GetObject **создает объект** устройства конечной точки, который представляет устройство, и предоставляет интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-148">**GetDevice** creates an endpoint device object to represent the device and provides the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface to that object.</span></span> <span data-ttu-id="8d6d8-149">Затем \_ принтдевиценаме вызывает метод [**иммдевице:: опенпропертисторе**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) , чтобы получить интерфейс **ипропертисторе** в хранилище свойств устройства.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-149">Next, \_PrintDeviceName calls the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to retrieve the **IPropertyStore** interface to the device's property store.</span></span> <span data-ttu-id="8d6d8-150">Наконец, \_ принтдевиценаме вызывает метод **ипропертисторе::-Item** для получения свойства понятного имени устройства.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-150">Finally, \_PrintDeviceName calls the **IPropertyStore::GetItem** method to obtain the friendly-name property of the device.</span></span> <span data-ttu-id="8d6d8-151">Дополнительные сведения о **ипропертисторе** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-151">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="8d6d8-152">В дополнение к событиям устройства клиенты могут регистрироваться для получения уведомлений о событиях звукового сеанса и событиях тома конечной точки.</span><span class="sxs-lookup"><span data-stu-id="8d6d8-152">In addition to device events, clients can register to receive notifications of audio-session events and endpoint-volume events.</span></span> <span data-ttu-id="8d6d8-153">Дополнительные сведения см. в разделе [**интерфейс иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) и [**интерфейс иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span><span class="sxs-lookup"><span data-stu-id="8d6d8-153">For more information, see [**IAudioSessionEvents Interface**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) and [**IAudioEndpointVolumeCallback Interface**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d6d8-154">См. также</span><span class="sxs-lookup"><span data-stu-id="8d6d8-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d6d8-155">Устройства конечных точек звука</span><span class="sxs-lookup"><span data-stu-id="8d6d8-155">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



