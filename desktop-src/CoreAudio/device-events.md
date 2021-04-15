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
# <a name="device-events-core-audio-apis"></a>События устройства (основные API-интерфейсы для аудиоподсистемы)

Событие устройства уведомляет клиентов об изменении состояния [устройства конечной точки аудио](audio-endpoint-devices.md) в системе. Ниже приведены примеры событий устройств.

-   Пользователь включает или отключает устройство звуковой конечной точки из диспетчер устройств или с помощью панели управления Windows мультимедиа Mmsys.cpl.
-   Пользователь добавляет звуковой адаптер в систему или удаляет звуковой адаптер из системы.
-   Пользователь подключает устройство аудио конечных точек к звуковой розетке с обнаружением разъема или удаляет устройство звуковой конечной точки с такого разъема.
-   Пользователь изменяет [роль устройства](device-roles.md) , назначенную устройству.
-   Значение [Свойства устройства](device-properties.md) изменяется.

Добавление или удаление звукового адаптера создает события устройства для всех устройств конечных точек аудио, подключающихся к адаптеру. Первые четыре элемента в приведенном выше списке являются примерами изменений состояния устройства. Дополнительные сведения о состояниях устройств конечных точек звука см. в разделе [Device \_ State \_ xxx константы](device-state-xxx-constants.md). Дополнительные сведения об обнаружении устройств с разъемами см. в статье [устройства конечных точек аудио](audio-endpoint-devices.md).

Клиент может зарегистрироваться, чтобы получать уведомления при возникновении событий устройства. В ответ на эти уведомления клиент может динамически изменить способ использования определенного устройства или выбрать другое устройство для использования в конкретной цели.

Например, если приложение воспроизводит звуковую дорожку через набор динамиков USB, и пользователь отключает динамики от USB-разъема, приложение получает уведомление о событии устройства. В ответ на событие, если приложение обнаруживает, что набор настольных динамиков подключен к интегрированному звуковому адаптеру на системной плате, приложение может возобновить воспроизведение звуковой дорожки через динамики рабочего стола. В этом примере переход от динамиков USB к динамикам настольных компьютеров происходит автоматически, не требуя от пользователя явного перенаправления приложения.

Чтобы зарегистрироваться для получения уведомлений устройства, клиент вызывает метод [**иммдевицеенумератор:: регистерендпоинтнотификатионкаллбакк**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) . Если клиенту больше не требуются уведомления, он отменяет их, вызывая метод [**иммдевицеенумератор:: унрегистерендпоинтнотификатионкаллбакк**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) . Оба метода принимают входной параметр с именем *пнотифи*, который является указателем на экземпляр интерфейса [**иммнотификатионклиент**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) .

Интерфейс **иммнотификатионклиент** реализуется клиентом. Интерфейс содержит несколько методов, каждый из которых служит подпрограммы обратного вызова для определенного типа события устройства. При возникновении события устройства в конечной точке звука модуль Ммдевице вызывает соответствующий метод в интерфейсе **иммнотификатионклиент** каждого клиента, зарегистрированного для получения уведомлений о событиях устройства. Эти вызовы передают описание события клиентам. Дополнительные сведения см. в разделе [**интерфейс иммнотификатионклиент**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).

Клиент, зарегистрированный для получения уведомлений о событиях устройства, будет получать уведомления обо всех типах событий устройств, происходящих во всех конечных устройствах аудио в системе. Если клиент заинтересован только в определенных типах событий или на определенных устройствах, то методы в его реализации **иммнотификатионклиент** должны соответствующим образом фильтровать события.

Windows SDK предоставляет примеры, включающие несколько реализаций для [**интерфейса иммнотификатионклиент**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient). Дополнительные сведения см. [в статье примеры пакетов SDK, в которых используются основные API аудио](sdk-samples-that-use-the-core-audio-apis.md).

В следующем примере кода показана возможная реализация интерфейса **иммнотификатионклиент** :


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



Класс Кммнотификатионклиент в предыдущем примере кода является реализацией интерфейса **иммнотификатионклиент** . Поскольку **иммнотификатионклиент** наследует от **IUnknown**, определение класса содержит реализации методов **IUnknown** , **AddRef**, **Release** и **QueryInterface**. Остальные открытые методы в определении класса относятся к интерфейсу **иммнотификатионклиент** . Этими методами являются:

-   **Ондефаултдевицечанжед**, который вызывается при изменении пользователем роли устройства конечной точки звука.
-   **Ондевицеаддед**, который вызывается, когда пользователь добавляет устройство конечной точки аудио в систему.
-   **Ондевицеремовед**, который вызывается, когда пользователь удаляет устройство конечной точки аудио из системы.
-   **Ондевицестатечанжед**, который вызывается при изменении состояния устройства для устройства конечной точки аудио. (Дополнительные сведения о состояниях устройств см. в разделе [Device \_ State \_ xxx константы](device-state-xxx-constants.md).)
-   **Онпропертивалуечанжед**, который вызывается при изменении значения свойства устройства конечной точки аудио.

Каждый из этих методов принимает входной параметр *пвстрдевицеид*, который является указателем на строку идентификатора конечной точки. Строка определяет устройство аудио конечной точки, в котором произошло событие устройства.

В предыдущем примере кода \_ принтдевиценаме является частным методом в классе кммнотификатионклиент, который выводит понятное имя устройства. \_Принтдевиценаме принимает строку идентификатора конечной точки в качестве входного параметра. Он передает строку в метод [**иммдевицеенумератор::**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) GetString. GetObject **создает объект** устройства конечной точки, который представляет устройство, и предоставляет интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) для этого объекта. Затем \_ принтдевиценаме вызывает метод [**иммдевице:: опенпропертисторе**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) , чтобы получить интерфейс **ипропертисторе** в хранилище свойств устройства. Наконец, \_ принтдевиценаме вызывает метод **ипропертисторе::-Item** для получения свойства понятного имени устройства. Дополнительные сведения о **ипропертисторе** см. в документации по Windows SDK.

В дополнение к событиям устройства клиенты могут регистрироваться для получения уведомлений о событиях звукового сеанса и событиях тома конечной точки. Дополнительные сведения см. в разделе [**интерфейс иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) и [**интерфейс иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устройства конечных точек звука](audio-endpoint-devices.md)
</dt> </dl>

 

 



